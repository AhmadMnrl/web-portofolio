<script>
export default {
  data() {
    return {
      activeTab: 1,
      tech: [
        {
          id: 1,
          name: 'HTML',
          imageUrl: 'https://cdn-icons-png.flaticon.com/512/1051/1051277.png',
          status: 'Advanced'
        },
        {
          id: 2,
          name: 'CSS',
          imageUrl: 'https://cdn-icons-png.flaticon.com/512/732/732190.png',
          status: 'Advanced'
        },
        {
          id: 3,
          name: 'PHP',
          imageUrl: 'https://cdn.iconscout.com/icon/free/png-256/free-php-2038871-1720084.png',
          status: 'Advanced'
        },
        {
          id: 4,
          name: 'Javascript',
          imageUrl: 'https://cdn.icon-icons.com/icons2/2415/PNG/512/javascript_original_logo_icon_146455.png',
          status: 'Intermediate'
        },
        {
          id: 5,
          name: 'Laravel',
          imageUrl: 'https://cdn.worldvectorlogo.com/logos/laravel-2.svg',
          status: 'Advance'
        },
        {
          id: 7,
          name: 'VueJS',
          imageUrl: 'https://cdn.iconscout.com/icon/free/png-256/free-vue-282497.png?f=webp',
          status: 'Beginner'
        },
        {
          id: 9,
          name: 'NodeJS',
          imageUrl: 'https://cdn.iconscout.com/icon/free/png-256/free-node-js-1174925.png',
          status: 'Beginner'
        },
        {
          id: 10,
          name: 'Tailwind',
          imageUrl: 'https://upload.wikimedia.org/wikipedia/commons/d/d5/Tailwind_CSS_Logo.svg',
          status: 'Beginner'
        },
        {
          id: 11,
          name: 'Bootstrap',
          imageUrl: 'https://getbootstrap.com/docs/5.2/assets/brand/bootstrap-logo-shadow.png',
          status: 'Intermediate'
        },
        {
          id: 12,
          name: 'ReactJS',
          imageUrl: 'https://cdn4.iconfinder.com/data/icons/logos-3/600/React.js_logo-512.png',
          status: 'Beginner'
        }
      ],
      tools: [
        {
          id: 1,
          name: 'Git',
          imageUrl: 'https://git-scm.com/images/logos/downloads/Git-Icon-1788C.png',
          status: 'Version Control'
        },
        {
          id: 2,
          name: 'GitHub',
          imageUrl: 'https://cdn-icons-png.flaticon.com/512/25/25231.png',
          status: 'Git Hosting'
        },
        {
          id: 3,
          name: 'NPM',
          imageUrl: 'https://cdn.iconscout.com/icon/free/png-256/free-npm-3-1175132.png',
          status: 'Package Manager'
        },
        {
          id: 4,
          name: 'MySQL',
          imageUrl: 'https://cdn-icons-png.flaticon.com/512/5968/5968313.png',
          status: 'Database'
        },
        {
          id: 5,
          name: 'MongoDB',
          imageUrl: 'data:image/png;base64,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',
          status: 'Database'
        },
        {
          id: 5,
          name: 'Laragon',
          imageUrl: 'data:image/jpeg;base64,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',
          status: 'Server Web'
        },
      ]
    };
  }
}
</script>
<template>
  <div
    class="bg-[#1e1e1f] px-5 py-5 md:px-12 md:py-10 text-left border border-[#383838] rounded-3xl text-amber-50 mx-3 mb-5">
    <article data-page="about">

      <header>
        <div class="text-2xl font-bold text-white mb-5 fadein-bot title-section flex items-center">
          About Me &nbsp;
          <div class="h-[1px] w-32 bg-amber-200 md:w-96 aos-init aos-animate" data-aos="zoom-in-left"
            data-aos-duration="600"></div>
        </div>
      </header>

      <section
        class="text-sm md:text-lg text-justify flex flex-col gap-4 md:flex-row md:gap-8 md:justify-left md:items-center">
        <div class="flex justify-center">
          <img class="w-9/12 rounded-full mb-3 fadein-up"
            src="../assets/arul.jpg" alt="Foto">
        </div>
        <div class="md:w-7/12">
          <p class="mb-3 md:mb-7 fadein-left fadeins-1">
            &nbsp; &nbsp; &nbsp; Hi Everyone! My name is Ahmad Manarul Baehaqi. I am a web developer from Depok, West Java. 
            I have 1 year experience in back-end web development. I really enjoy what I am doing at the moment, 
            in my opinion making programs is not just a job, but also an art that has aesthetic value.
          </p>
          <p class="mb-3 fadein-left fadeins-2">
            &nbsp; &nbsp; &nbsp; My job is to build your website to be functional and user-friendly yet still attractive.
            In addition, I provide a personal touch to your product and ensure that the website catches attention and is
            easy to use.
            My goal is to convey your message and identity in the most creative way. If you are interested in hiring me,
            please contact the listed contact.
          </p>
        </div>

      </section>

    </article>
  </div>

  <div class="px-5 py-5 md:px-12 md:py-10 text-left text-amber-50 mx-3">
    <article data-page="about">
      <header>
        <div class="text-2xl font-bold text-white mb-5 fadein-bot title-section flex items-center">
          <div class="h-[1px] w-10 bg-amber-200 md:w-20 aos-init aos-animate" data-aos="zoom-in-left"
            data-aos-duration="600"></div>
          &nbsp; Skills
        </div>
      </header>
      <section>
        <div>
          <ul class="flex flex-wrap text-sm font-medium text-center text-gray-500 dark:text-gray-400 mb-5">
            <li class="mr-2">
              <button class="inline-block px-4 py-3 rounded-lg hover:text-white"
                :class="{ 'text-amber-200 bg-amber-200 bg-opacity-10': activeTab === 1 }" @click="activeTab = 1">Tech Stack</button>
            </li>
            <li class="mr-2">
              <button class="inline-block px-4 py-3 rounded-lg hover:text-white"
                :class="{ 'text-amber-200 bg-amber-200 bg-opacity-10': activeTab === 2 }" @click="activeTab = 2">Tools</button>
            </li>
          </ul>
        </div>
        <div v-show="activeTab === 1">
          <div class="grid grid-cols-2 gap-4 pb-32 md:grid-cols-3 md:gap-8 xl:grid-cols-4 xl:gap-10 2xl:gap-12">
            <div v-for="item in tech" :key="item.id">
              <div
                class="item-tech flex cursor-pointer items-center gap-2 rounded border border-amber-200 px-2 py-2 hover:bg-amber-200 hover:bg-opacity-10 md:gap-3 lg:px-3">
                <div class="flex h-12 w-12 items-center justify-center p-0 lg:h-16 lg:w-16 lg:p-2 zoom-in">
                  <img alt="HTML" loading="lazy" width="32" height="32" decoding="async" data-nimg="1"
                    class="img-tech drop-shadow-xl transition-all duration-300 h-[65%] w-[65%] lg:h-[85%] lg:w-[85%]  "
                    :src="item.imageUrl" style="color: transparent;">
                </div>
                <div class="flex items-center text-sm md:text-base lg:text-lg">
                  <div class="tech font-medium text-secondary transition-all duration-300 translate-y-0 ">{{ item.name }}
                  </div>
                  <div
                    class="status-tech opacity-0 absolute mt-5 text-[10px] text-amber-200 transition-all duration-300 md:text-xs lg:text-sm">
                    {{ item.status }}</div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div v-show="activeTab === 2">
          <div class="grid grid-cols-2 gap-4 pb-32 md:grid-cols-3 md:gap-8 xl:grid-cols-4 xl:gap-10 2xl:gap-12">
            <div v-for="item in tools" :key="item.id">
              <div
                class="item-tech flex cursor-pointer items-center gap-2 rounded border border-amber-200 px-2 py-2 hover:bg-amber-200 hover:bg-opacity-10 md:gap-3 lg:px-3">
                <div class="flex h-12 w-12 items-center justify-center p-0 lg:h-16 lg:w-16 lg:p-2 zoom-in">
                  <img alt="HTML" loading="lazy" width="32" height="32" decoding="async" data-nimg="1"
                    class="img-tech drop-shadow-xl transition-all duration-300 h-[65%] w-[65%] lg:h-[85%] lg:w-[85%]  "
                    :src="item.imageUrl" style="color: transparent;">
                </div>
                <div class="flex items-center text-sm md:text-base lg:text-lg">
                  <div class="tech font-medium text-secondary transition-all duration-300 translate-y-0 ">{{ item.name }}
                  </div>
                  <div
                    class="status-tech opacity-0 absolute mt-5 text-[10px] text-amber-200 transition-all duration-300 md:text-xs lg:text-sm">
                    {{ item.status }}</div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
    </article>
  </div>
</template>

<style>
.fadein-left {
  opacity: 0;
  animation: fadeInLeft 0.5s ease-out forwards;
}

@keyframes fadeInLeft {
  0% {
    opacity: 0;
    transform: translateX(100%);
  }

  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

.fadeins-1 {
  animation-delay: 500ms;
}

.fadeins-2 {
  animation-delay: 800ms;
}

.img-tech,
.tech {
  transition: transform 0.3s ease;
}

.item-tech:hover .img-tech {
  transform: scale(1.3);
}

.item-tech:hover .tech {
  transform: translateY(-12px);
}

.item-tech:hover .status-tech {
  opacity: 1;
}
</style>
