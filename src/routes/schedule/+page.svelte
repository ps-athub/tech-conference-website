<script>
// @ts-nocheck

    let selectedFilter = "All";

    const schedule = [
        { date: "Aug 15", time: "10:00 AM", topic: "Opening Keynote", speaker: "Sundar Pichai", track: "Main Stage" },
        { date: "Aug 15", time: "12:00 PM", topic: "The Future of AI", speaker: "Narayana Murthy", track: "AI & ML" },
        { date: "Aug 15", time: "02:00 PM", topic: "Cybersecurity in 2025", speaker: "Nandan Nilekani", track: "Security" },
        { date: "Aug 16", time: "11:00 AM", topic: "Blockchain & Web3", speaker: "Vitalik Buterin", track: "Blockchain" },
        { date: "Aug 16", time: "01:00 PM", topic: "Cloud Innovations", speaker: "Satya Nadella", track: "Cloud Computing" },
        { date: "Aug 17", time: "10:30 AM", topic: "Women in Tech Panel", speaker: "Kiran Mazumdar-Shaw", track: "Diversity & Inclusion" }
    ];

    function filterSchedule(item) {
        return selectedFilter === "All" || item.date === selectedFilter || item.track === selectedFilter;
    }
</script>

<div class="container py-5">
    <h2 class="text-center mb-4">Conference Schedule</h2>

    <!-- Filter Buttons -->
    <div class="filter-buttons">
        <button on:click={() => (selectedFilter = "All")} class:selected={selectedFilter === "All"}>All</button>
        <button on:click={() => (selectedFilter = "Aug 15")} class:selected={selectedFilter === "Aug 15"}>Aug 15</button>
        <button on:click={() => (selectedFilter = "Aug 16")} class:selected={selectedFilter === "Aug 16"}>Aug 16</button>
        <button on:click={() => (selectedFilter = "Aug 17")} class:selected={selectedFilter === "Aug 17"}>Aug 17</button>
    </div>

    <div class="schedule-container">
        <table class="schedule-table">
            <thead>
                <tr>
                    <th>Date</th>
                    <th>Time</th>
                    <th>Topic</th>
                    <th>Speaker</th>
                    <th>Track</th>
                </tr>
            </thead>
            <tbody>
                {#each schedule.filter(filterSchedule) as session}
                <tr>
                    <td>{session.date}</td>
                    <td>{session.time}</td>
                    <td>{session.topic}</td>
                    <td>{session.speaker}</td>
                    <td>{session.track}</td>
                </tr>
                {:else}
                <tr>
                    <td colspan="5" class="no-sessions">No sessions available for this selection</td>
                </tr>
                {/each}
            </tbody>
        </table>
    </div>
</div>

<style>
/* Container Styling */
.schedule-container {
    background: #ffffff;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
    overflow-x: auto;
}

/* Table Styling */
.schedule-table {
    width: 100%;
    border-collapse: collapse;
    text-align: left;
    font-size: 1rem;
    border-radius: 8px;
}

.schedule-table thead {
    background: #007bff;
    color: white;
}

.schedule-table th, 
.schedule-table td {
    padding: 15px;
    border-bottom: 1px solid #ddd;
}

.schedule-table tbody tr:hover {
    background: #f8f9fa;
}

/* Filter Buttons */
.filter-buttons {
    text-align: center;
    margin-bottom: 20px;
}

.filter-buttons button {
    background: #007bff;
    color: white;
    border: none;
    padding: 10px 20px;
    margin: 5px;
    font-size: 1rem;
    cursor: pointer;
    border-radius: 5px;
    transition: all 0.3s ease;
}

.filter-buttons button:hover,
.filter-buttons button.selected {
    background: #0056b3;
}

/* No Sessions Message */
.no-sessions {
    text-align: center;
    font-style: italic;
    color: #888;
}
</style>
