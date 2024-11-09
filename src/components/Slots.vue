<template>
    <div class="componente">
        <h1>Slots</h1>
        <button> 
            <slot name="icone"></slot>
            <slot name="texto">
                Default
            </slot>
        </button>
    </div>
</template>