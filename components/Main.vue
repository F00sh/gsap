<template>
    <div class="relative -z-2 bg-black flex w-full h-screen items-center justify-start">
        <div ref="squeezeText" id="main_title" class="flex w-full h-full justify-start items-start bg-[url(/public/png/screen_orange.png)] bg-no-repeat p-10 text-center bg-auto mt-60 pt-55 pl-60">

        </div>
        <div class="absolute flex w-3/4 h-full justify-between items-start bg-no-repeat p-10 text-center bg-auto mt-110 pt-55 pl-60">
            <div class="mt-20">
                <h1 class="text-white text-[5.1rem] font-semibold uppercase tracking-[0.35rem]">Marko Vilipić</h1>
                <ul class="flex text-[4rem] tracking-[0.5rem]">
                    <h1 class="text-red-400 font-semibold uppercase">design</h1>
                    <h1 class="text-green-400 font-semibold uppercase">-art-</h1>
                    <h1 class="text-blue-400 font-semibold uppercase">web</h1>
                </ul>
            </div>
            <p class="text-white text-md font-light tracking-[0.25rem] mt-4 w-2/5">
                As a versatile product designer, I specialize in game design, animation, web design, and more.<br> 
                With a bachelor's degree in product design and a solid foundation in art and design, 
                I am equipped to deliver high-quality services in product and graphic design, 3D modeling, 
                2D/3D animation, web design, UI/UX, and video game asset modeling and mechanics design.<br> 
                I am proficient in using Adobe Creative Suite, Blender, HTML & CSS, Figma, Revit, and AutoCAD.<br> 
                I am eager to collaborate with steady clients who value creativity and precision in their projects. 
                Based in Croatia, I am ready to bring your vision to life with innovative and effective design solutions.
            </p>
        </div>
    </div>
</template>

<script setup lang="ts">
import { onMounted, ref } from 'vue'
import gsap from 'gsap'

const squeezeText = ref<HTMLElement | null>(null)

onMounted(() => {
  if (squeezeText.value) {
    gsap.to(squeezeText.value, {
      scaleY: 0.9,
      transformOrigin: 'center',
      duration: 2,
      ease: 'power2.inOut',
      yoyo: true,
      repeat: -1
    })
  }
})
</script>