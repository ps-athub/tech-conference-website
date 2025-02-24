India Tech Conference 2025 - Website

Welcome to the India Tech Conference 2025 website repository! This modern, responsive website is built using SvelteKit and Bootstrap, designed to provide information about speakers, schedules, sponsors, and registration for the conference.

📌 Features	

✅ Responsive Navbar – Modern, mobile-friendly navigation bar	

✅ Hero Section with Countdown Timer – Displays time remaining until the conference starts	

✅ Event Schedule with Filters – Buttons to filter sessions by day	

✅ Speakers Page with Grid Layout – Showcases all speakers with their names, images, and bios	

✅ Sponsors Page with Tiers – Categorizes sponsors into Gold, Silver, and Bronze tiers	

✅ Location Details with Embedded Google Map – Displays conference venue information	

✅ Contact Form – Users can send inquiries via the built-in contact form	

✅ Dark-Themed Footer – Social media links with improved aesthetics	

 

	
 📄 Pages Implemented		
 1. Home Page

    A hero section with the conference name, tagline, and a “Register Now” button.

    A featured section highlighting keynote speakers (with images, names, and titles).		
	
3. Speakers Page

   A grid layout showcasing all speakers with their names, images, titles, and short bios.		
	
3. Schedule Page

   A structured timetable of the conference sessions (date, time, topic, speaker).

   Tabs or buttons to filter sessions by day or track.		
	
4. Sponsors Page

   List of sponsors with logos and links, categorized by Gold, Silver, and Bronze tiers.		
	
5. About Page

   A brief introduction to the conference, its purpose, and what attendees can expect.		
	
6. Contact Page

   A contact form (Name, Email, Message) for user inquiries.

   Social media links for easy connection.	
	

 
	
 📂 Project Setup	

1️. Clone the Repository		
	
 	git clone https://github.com/ps-athub/tech-conference-website.git	
 	
	cd tech-conference-website		
	 
	 
2️. Install Dependencies	
	
    npm install		
	 
	 
3️. Start Development Server	
	
    npm run dev	
	 
   Your website will now be running locally at http://localhost:5173/ (default port for SvelteKit)	
	 

----------------------------------------------------------------------------------------------------------------------------------------------------------------

# sv

Everything you need to build a Svelte project, powered by [`sv`](https://github.com/sveltejs/cli).

## Creating a project

If you're seeing this, you've probably already done this step. Congrats!

```bash
# create a new project in the current directory
npx sv create

# create a new project in my-app
npx sv create my-app
```

## Developing

Once you've created a project and installed dependencies with `npm install` (or `pnpm install` or `yarn`), start a development server:

```bash
npm run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

## Building

To create a production version of your app:

```bash
npm run build
```

You can preview the production build with `npm run preview`.

> To deploy your app, you may need to install an [adapter](https://svelte.dev/docs/kit/adapters) for your target environment.
