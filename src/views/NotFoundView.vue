<template>
    <div class="error-container">
        <div class="error-code">404</div>
        <div class="error-message">Página no encontrada</div>
        <p>Lo sentimos, la página que estás buscando no existe.</p>
        <a href="/" class="btn btn-primary">Volver a la página de inicio</a>
    </div>
</template>

<style>

.error-container {
            text-align: center;
        }

        .error-code {
            font-size: 120px;
            font-weight: bold;
            color: #dc3545; /* Color de alerta en Bootstrap */
        }

        .error-message {
            font-size: 24px;
            margin-top: 20px;
        }

</style>