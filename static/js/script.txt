// =============================
// SCRIPT PRINCIPAL – SOS CNH
// Mobile First | One Page
// =============================

// Garantia de rolagem suave para âncoras

document.addEventListener('DOMContentLoaded', function () {
    const links = document.querySelectorAll('a[href^="#"]');

    links.forEach(link => {
        link.addEventListener('click', function (e) {
            const targetId = this.getAttribute('href');
            const targetElement = document.querySelector(targetId);

            if (targetElement) {
                e.preventDefault();
                const offsetTop = targetElement.offsetTop;

                window.scrollTo({
                    top: offsetTop - 10,
                    behavior: 'smooth'
                });
            }
        });
    });
});

// Nenhuma lógica extra aplicada neste momento
// Script mantido simples conforme escopo aprovado
