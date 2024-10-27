<script>
  import Step from "./Step.svelte";

  let steps = [
    {name: 'Chess Engine', icon: 'fa-solid fa-chess', href: 'https://github.com/sahandp2012p/chess_engine'},
    {name: 'YouTube Comments', icon: 'fa-brands fa-youtube', href: 'https://github.com/sahandp2012p/youtube_comments'},
    {name: 'Data analysis on YouTube Videos', icon: 'fa-brands fa-youtube', href: 'https://github.com/sahandp2012p/data-analysis'},
    {name: 'Eta Calculator', icon: 'fa-solid fa-clock', href: 'https://github.com/sahandp2012p/icds-project'},
  ]

  let benefits = [
    {name: 'a self taught developer', decsription: 'I am a completely self-taught developer and have not taken any courses. I\'m a Full Stack developer and also have tons of experience in Data Science'},
    {name: 'a multilingual developer', decsription: 'I can fluently speak in 7 languages! Includuding: Persian, English, Turkish, French (DELF Prim A2.2 92.5/100), German, Itailan (CILS Bambini A2 53/60) and Spanish. And I\'m currently learning Arabic and Russian!'},
    {name: 'awards', decsription: 'I have a lot of Awards! I have a Bronze medal at the SASMO Math olympiad and have a gold medal at the SIMOC Math olympiad! I also have a Silver medal in the Avicenna Research Center Festival! I also have a GCPA Award (Global Child Prodigy Awards) and I\'m also part of the Mensa High IQ Society with 146 points!'},
  ]
</script>

<main class="flex flex-col flex-1 p-4">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
        <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
            <h2 class="font-semibold text4xl sm:text-5xl md:text-6xl">
                Hi, I'm <span class="poppins text-violet-400">Sahand</span> Pourjavad <br /> Full Stack <span class="poppins text-violet-400">Developer</span> & <span class="poppins text-violet-400">Data</span> Scientist
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                My <span class="text-violet-400">favorite tech</span> includes Python, FastAPI, ScikitLearn, TensorFlow, JavaScript, SvelteKit, ReactJS, Sass, TailwindCSS and Vite!
            </p>
            <a href="mailto:sahndpourjavad@gmail.com" target="_blank" class="blueShadow mx-auto lg:mr-auto text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer">
                <div class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full-z-0 duration-200" />
                <h4 class="relative z-9">Get in touch &rarr;</h4>
            </a>
        </div>
        <div class="relative shadow-2xl grid place-items-center">
            <img src={"images/profile.jpg"} alt="Profile Image" class="rounded-full object-cover z-[2] max-h-[70h]">
        </div>
    </section>
    <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-large sm:text-xl md:text2xl">
                A few of my creative endeavors.
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Curious to <span class="poppins text-violet-400">see</span> my work?
            </h3>
        </div>
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>A simple chess engine that has it's own interface to play against. Created with
                <strong class="text-violet-400">Pygame and Python-Chess!</strong> Pygame is used for the interface of the game and Python-Chess is used to create the engine 
                </p>        
                <br>
                <br>
            </Step>
            <Step step={steps[1]}>
                <p>An application that analyzes a YouTube video's comments and gives a score from 1 to 10. Built with <strong class="text-violet-400">FastAPI SQLite NLTK and Vite!</strong> FastAPI is used to create the API for the backend and SQLite is used for the DataBase. NLTK is used for the sentiment analysis. Vite is used for the website!</p>
                <br>
            </Step>
            <Step step={steps[2]}>
                <p>A data analysis on YouTube videos (Views, Titles, etc.) That also has a WordCloud! Crafted with <strong class="text-violet-400">Pandas Numpy and WordCloud!</strong> Pandas is used for loading the data and working with the dataset. Numpy for numeric Calculations and WordCloud for creating the WordCloud!</p>
            </Step>

            <Step step={steps[3]}>
                <p>A project that calculates the ETA's of routes using Dijkstra's Algorithm. Created with <strong class="text-violet-400">NetworkX Pandas Numpy Scikit-learn XGBoost and LightGBM!</strong> NetworkX for Graphs. Numpy for Numerical Calcuations. Scikit-learn, XGBoost and LighGBM for Models!</p>
            </Step>
        </div>
    </section>
    <section id="about" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative">
        <div class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4">
        <h6 class="text-lg sm:text-xl md:text-2xl">Want to know more?</h6>
        <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">A bit <span class="poppins text-violet-400">about</span> me.</h3>
        </div>
        <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">I am . . .</p>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
            {#each benefits as benefit, index}
            <div class="flex gap-6 sm:gap-8">
                <p class="poppins tet-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold">
                    0{index+1}
                </p>
                <div class="flex flex-col gap-6 sm:gap-8">
                    <h3 class="text-2xl sm:text-3xl md:text-5xl">
                        {benefit.name}
                    </h3>
                    <p>{benefit.decsription}</p>
                </div>
            </div>
            {/each}
        </div>
        <h5 class="text-2xl sm:textl-3xl font-semibold text-center poppins">The <span class="text-violet-400 poppins">Complete</span> Package</h5>
        <div class="flex flex-col overflow-x-scroll gap-10 max-w-[800px] mx-auto w-full">
            <table class="bg-white text-slate-700 rounded text-center">
                <thead class="border-b border-solid border-slate-200">
                    <tr class="">
                        <th />
                        <th class="whitespace-nowrap p-2 px-4">Candidate #1</th>
                        <th class="whitespace-nowrap p-2 px-4">Candidate #2</th>
                        <th class="whitespace-nowrap p-2 px-4">Candidate #3</th>
                        <th class="whitespace-nowrap bg-violet-700 text-white p-4 px-8">Me</th>
                    </tr>
                </thead>
                <tbody>
                    <tr class="border-b border-solid border-slate-200">
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm">Dedication</td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-green-500"></i></td>
                    </tr>
                    <tr class="border-b border-solid border-slate-200">
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm">Critical Thought</td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-green-500"></i></td>
                    </tr>
                    <tr class="border-b border-solid border-slate-200">
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm">Interpersonal Skills</td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-green-500"></i></td>
                    </tr>
                    <tr class="border-b border-solid border-slate-200">
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm">Programming Ability</td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-green-500"></i></td>
                    </tr>
                </tbody>
            </table>
        </div>
        <div class="mx-auto -mt-12 italic sm:hidden opacity-50">
            <p>Scroll to see more &rarr;</p>
        </div>
        <p class="mx-auto">So why not invest?</p>
    </section>
</main>
