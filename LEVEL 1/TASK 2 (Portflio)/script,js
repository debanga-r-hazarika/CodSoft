
gsap.registerPlugin(ScrollTrigger);

gsap.from('nav', {
    y: -100,
    opacity: 0,
    duration: 1,
    ease: 'power3.out'
});

gsap.utils.toArray('section').forEach((section, i) => {
    gsap.from(section, {
        y: 50,
        opacity: 0,
        duration: 1,
        scrollTrigger: {
            trigger: section,
            start: 'top 80%',
            end: 'top 20%',
            scrub: 1,
        }
    });
});

gsap.utils.toArray('.skill-tag').forEach((tag, i) => {
    gsap.from(tag, {
        scale: 0,
        opacity: 0,
        duration: 0.5,
        delay: i * 0.1,
        scrollTrigger: {
            trigger: '#skills',
            start: 'top 80%',
        }
    });
});

gsap.utils.toArray('.project').forEach((project, i) => {
    gsap.from(project, {
        y: 50,
        opacity: 0,
        duration: 1,
        scrollTrigger: {
            trigger: project,
            start: 'top 80%',
        }
    });
});

// Lottie animations
const lottieAnimations = [
    { containerId: 'lottie-home', path: 'https://assets2.lottiefiles.com/packages/lf20_kkflmtur.json' },
    { containerId: 'lottie-about', path: 'https://assets3.lottiefiles.com/private_files/lf30_WdTEui.json' },
    { containerId: 'lottie-experience', path: 'https://assets2.lottiefiles.com/packages/lf20_bp5lntrf.json' },
    { containerId: 'lottie-contact', path: 'https://assets4.lottiefiles.com/packages/lf20_u25cckyh.json' }
];

lottieAnimations.forEach(animation => {
    lottie.loadAnimation({
        container: document.getElementById(animation.containerId),
        renderer: 'svg',
        loop: true,
        autoplay: true,
        path: animation.path
    });
});

// Typing animation for the name
const nameElement = document.querySelector('h1');
const nameText = nameElement.textContent;
nameElement.textContent = '';
for (let i = 0; i < nameText.length; i++) {
    const span = document.createElement('span');
    span.textContent = nameText[i];
    span.style.opacity = '0';
    nameElement.appendChild(span);
    gsap.to(span, {
        opacity: 1,
        duration: 0.1,
        delay: i * 0.1
    });
}
