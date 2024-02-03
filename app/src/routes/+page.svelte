<script>
    /**
     * @param {HTMLHeadingElement} element
     */
    const headerLoadAnimation = element => {
        const text = 'TIỆN LỢI - GIÁ RẺ - NHANH GỌN';

        element.textContent = '';
        element.style.opacity = '1';
        for(let i = 0; i < text.length; i++) {
            const child = document.createElement('p');
                const char = text.charAt(i);
                child.textContent = char;
                if(char === ' ') {
                    child.textContent = '0';
                    child.style.opacity = '0';
                }
                element.appendChild(child);
            setTimeout(() => {
                child.classList.add('show');
            },(Math.abs(text.length/2 - i))*50);
        }
    }
    /**
     * @param {HTMLHeadingElement} element
     */
    const descriptionLoadAnimation = element => {
        setTimeout(() => {
            element.style.opacity = '1';
        }, 800);
    }
</script>

<nav>
    <img src='favicon.jpeg' alt='logo'>
</nav>

<section id='hero-section'>
    <img alt=' ' src='heroImage.jpeg'>
    <h1 use:headerLoadAnimation>
        TIỆN LỢI - GIÁ RẺ - NHANH GỌN
    </h1>
    <h2 use:descriptionLoadAnimation>Đáp ứng mọi nhu cầu sống hằng ngày của bạn</h2>
</section>

<style src='./style.css' global></style>
