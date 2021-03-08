# My CV

### Introducing  
Hi! My name is Nikolay Arbuzov  

### Motivation ?  
For the last four years I have worked in retail companies, closely related to process management and having an active position to improve and optimize processes improved anything on my own, in my field and also made suggestions for improvement if the participation of a related department was required. But the overall result of the implementation did not suit me since there is bureaucracy, and a conservative attitude towards any new ideas and for myself, I did not find growth in that environment.  

I think, the desire to work in IT is associated with the easier the transformation of an idea into a product, a large community and the presence of charged people who can be like-minded people for me

### Skills  
In four years of working with data, I discovered the ability to analyze data, process analysis, business analysis, process automation, automation of human activities in the workplace, writing scripts with a high return on investment, writing technical tasks, understanding and solving problems of people in the workplace, data visualization, increasing the ergonomics and ecology of existing processes, creation of ergonomic and eco-friendly processes. This can all be attributed to Soft-skills.  

My Hard-skills are VBA, SQL, JS, Python, React, OOP, Unit-Testing, Debugging

### Examples of code  
As a code example, I will give a self-written fragment of a possible strategy-game that draws a frame to select units.
This fragment also uses a helper-function to find an element with a specific attribute.
A click-eventlistener is added to the playing field, and after the click, an eventlistener for the mouse movement is added, and an additional semi-transparent div-element appears, redrawn when the moving-mouse is held down. The logic of the main function provides work in any direction of mouse movement, adaptively changing the bearing points of the drawn frame. When you release the click, the frame disappears. Unfortunately, it was not possible to implement the removal of the listener for the movement of the mouse, as it is proposed in popular sources, and while the removal of the listener is carried out by removing the playing field and replacing it with the same, new one. 

    let changeFrame = (e,x,y)=>{
        let el = findEl('Рамка');
        if(e.clientX < x){
            el.style.left = `${e.clientX}px`;
            el.style.width = `${x-e.clientX}px`;
        } else {
            el.style.left = `${x}px`;
            el.style.width = `${e.clientX-x}px`;
        }
        if(e.clientY < y){
            el.style.top = `${e.clientY}px`;
            el.style.height = `${y-e.clientY}px`;
        } else {
            el.style.top = `${y}px`;
            el.style.height = `${e.clientY-y}px`;
        }
    }

    findEl('Игровое поле').addEventListener('mousedown', (e)=>{
        let x = e.clientX;
        let y = e.clientY;
        let frameField = new Block('Рамка',0,0,'RGBA(0,0,0,0.1)',y,x);
        frameField.render();
        findEl('Рамка').addEventListener('mousemove', (e)=>{changeFrame(e,x,y)})
        findEl('Игровое поле').addEventListener('mousemove', (e)=>{changeFrame(e,x,y)})
    })

    findEl('Игровое поле').addEventListener('mouseup', ()=>{
        findEl('Рамка').remove();
        findEl('Игровое поле').remove();
        let field = new Block('Игровое поле', window.innerWidth, window.innerHeight-100, 'green');
        field.altRender();
    })

### Experience  
Cumulative experience, I would roughly estimate as 800-1000 hours - like taking courses, doing homework, solving tasks on codewars (and others), solving work tasks, writing macros, scripts, automating dashboards

### Education  
I have an ordinary higher education in the specialty "Finance and Credit".
But I also took a lot of courses: face-to-face courses - "Forex", "Software Testing", "Pre-course on frontend", "Course on native JS", "React". Online Courses - "SQL / Advanced SQL", "OOP in JS", "NodeJS Basics".

### My English level  
I have approximately A2-level(pre-intermediate), read and translate, understand a little by ear and speak a little.  
My practice - I attended an English camp in childhood and in childhood completed the game Fallout 2 in English, with a dictionary, playing for the first time (in the game of all dialogues and inscriptions - 400k words)
