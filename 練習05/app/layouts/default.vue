<style>
body {
  margin: 0;
}

.header {
  display: grid;
  grid-template-columns: 1fr auto 1fr;
  align-items: center;

  margin-left: auto;
  margin-right: auto;
  margin-top: 20px;

  width: 1340px;
  height: auto;
}

.community {
  display: flex;
  align-items: center;
  justify-self: start
}

.icon {
  display: flex;
  align-items: center;
  justify-content: center;
  margin-right: 2px;

  width: 28px;
  height: 28px;
  padding: 5px;

  border-radius: 50%;
}

.logo-link {
  justify-self: center;
  line-height: 0;
}

.logo {
  display: block;
  width: 150px;
  height: auto;
}

.search {
  display: flex;
  align-items: center;
  justify-self: end;

  width: 28px;
  height: 28px;
  padding: 5px 2px 5px 8px;

  border-radius: 50%;
}

.label {
  display: flex;
  justify-content: center;
  margin-top: 18px;
  height: 54px;
  width: auto;

  gap: 36px;
  background-color: #000;
}

.label p {
  text-align: center;
  font-weight: 500;
  letter-spacing: 4px;
  word-spacing: 2px;

  color: #fff;
  font-size: 16px;
}

.breadcrumb-end {
  background-color: #f4f4f5;
  width: auto;
  height: 30px;
}


.breadcrumb {
  display: flex;
  align-items: center;
  justify-content: start;

  margin-left: auto;
  margin-right: auto;

  list-style: none;
  height: 30px;
  width: 1260px;
  padding: 0;

  font-size: 14px;
}

.breadcrumb-item+.breadcrumb-item::before {
  content: ">";
  margin: 21px 21px;
  color: #b5b5b5;
}

.breadcrumb-item a {
  text-decoration: none;
  color: #000;
}

.breadcrumb-item.active {
  color: #000;
  pointer-events: none;
  /* 當前頁面不可點擊 */
}

.page-all {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  width: 1260px;
  margin: 0 auto;
}

.page-left {
  display: flex;
  flex-direction: column;
  width: 900px;
  min-width: 0;
}

.page-right {
  display: flex;
  justify-content: center;
  width: 320px;
  flex-shrink: 0;
}
</style>

<template>

  <div class="header">

    <div class="community">

      <span class="icon">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24" fill="currentColor">
          <g>
            <path fill="none" d="M0 0h24v24H0z"></path>
            <path
              d="M14 13.5h2.5l1-4H14v-2c0-1.03 0-2 2-2h1.5V2.14c-.326-.043-1.557-.14-2.857-.14C11.928 2 10 3.657 10 6.7v2.8H7v4h3V22h4v-8.5z">
            </path>
          </g>
        </svg>
      </span>

      <span class="icon">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24" fill="currentColor">
          <g>
            <path fill="none" d="M0 0h24v24H0z"></path>
            <path fill-rule="nonzero"
              d="M12 9a3 3 0 1 0 0 6 3 3 0 0 0 0-6zm0-2a5 5 0 1 1 0 10 5 5 0 0 1 0-10zm6.5-.25a1.25 1.25 0 0 1-2.5 0 1.25 1.25 0 0 1 2.5 0zM12 4c-2.474 0-2.878.007-4.029.058-.784.037-1.31.142-1.798.332-.434.168-.747.369-1.08.703a2.89 2.89 0 0 0-.704 1.08c-.19.49-.295 1.015-.331 1.798C4.006 9.075 4 9.461 4 12c0 2.474.007 2.878.058 4.029.037.783.142 1.31.331 1.797.17.435.37.748.702 1.08.337.336.65.537 1.08.703.494.191 1.02.297 1.8.333C9.075 19.994 9.461 20 12 20c2.474 0 2.878-.007 4.029-.058.782-.037 1.309-.142 1.797-.331.433-.169.748-.37 1.08-.702.337-.337.538-.65.704-1.08.19-.493.296-1.02.332-1.8.052-1.104.058-1.49.058-4.029 0-2.474-.007-2.878-.058-4.029-.037-.782-.142-1.31-.332-1.798a2.911 2.911 0 0 0-.703-1.08 2.884 2.884 0 0 0-1.08-.704c-.49-.19-1.016-.295-1.798-.331C14.925 4.006 14.539 4 12 4zm0-2c2.717 0 3.056.01 4.122.06 1.065.05 1.79.217 2.428.465.66.254 1.216.598 1.772 1.153a4.908 4.908 0 0 1 1.153 1.772c.247.637.415 1.363.465 2.428.047 1.066.06 1.405.06 4.122 0 2.717-.01 3.056-.06 4.122-.05 1.065-.218 1.79-.465 2.428a4.883 4.883 0 0 1-1.153 1.772 4.915 4.915 0 0 1-1.772 1.153c-.637.247-1.363.415-2.428.465-1.066.047-1.405.06-4.122.06-2.717 0-3.056-.01-4.122-.06-1.065-.05-1.79-.218-2.428-.465a4.89 4.89 0 0 1-1.772-1.153 4.904 4.904 0 0 1-1.153-1.772c-.248-.637-.415-1.363-.465-2.428C2.013 15.056 2 14.717 2 12c0-2.717.01-3.056.06-4.122.05-1.066.217-1.79.465-2.428a4.88 4.88 0 0 1 1.153-1.772A4.897 4.897 0 0 1 5.45 2.525c.638-.248 1.362-.415 2.428-.465C8.944 2.013 9.283 2 12 2z">
            </path>
          </g>
        </svg>
      </span>

      <span class="icon">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24" fill="currentColor">
          <g>
            <path fill="none" d="M0 0h24v24H0z"></path>
            <path
              d="M21.543 6.498C22 8.28 22 12 22 12s0 3.72-.457 5.502c-.254.985-.997 1.76-1.938 2.022C17.896 20 12 20 12 20s-5.893 0-7.605-.476c-.945-.266-1.687-1.04-1.938-2.022C2 15.72 2 12 2 12s0-3.72.457-5.502c.254-.985.997-1.76 1.938-2.022C6.107 4 12 4 12 4s5.896 0 7.605.476c.945.266 1.687 1.04 1.938 2.022zM10 15.5l6-3.5-6-3.5v7z">
            </path>
          </g>
        </svg>
      </span>

      <span class="icon">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24" fill="currentColor">
          <g>
            <path fill="none" d="M0 0h24v24H0z"></path>
            <path fill-rule="nonzero"
              d="M18.663 10.84a.526.526 0 0 1-.526.525h-1.462v.938h1.462a.525.525 0 1 1 0 1.049H16.15a.526.526 0 0 1-.522-.524V8.852c0-.287.235-.525.525-.525h1.988a.525.525 0 0 1-.003 1.05h-1.462v.938h1.462c.291 0 .526.237.526.525zm-4.098 2.485a.538.538 0 0 1-.166.025.515.515 0 0 1-.425-.208l-2.036-2.764v2.45a.525.525 0 0 1-1.047 0V8.852a.522.522 0 0 1 .52-.523c.162 0 .312.086.412.211l2.052 2.775V8.852c0-.287.235-.525.525-.525.287 0 .525.238.525.525v3.976a.524.524 0 0 1-.36.497zm-4.95.027a.526.526 0 0 1-.523-.524V8.852c0-.287.236-.525.525-.525.289 0 .524.238.524.525v3.976a.527.527 0 0 1-.526.524zm-1.53 0H6.098a.528.528 0 0 1-.525-.524V8.852a.527.527 0 0 1 1.05 0v3.45h1.464a.525.525 0 0 1 0 1.05zM12 2.572c-5.513 0-10 3.643-10 8.118 0 4.01 3.558 7.369 8.363 8.007.325.068.769.215.881.492.1.25.066.638.032.9l-.137.85c-.037.25-.2.988.874.537 1.076-.449 5.764-3.398 7.864-5.812C21.313 14.089 22 12.477 22 10.69c0-4.475-4.488-8.118-10-8.118z">
            </path>
          </g>
        </svg>
      </span>

    </div>

    <NuxtLink to="/" class="logo-link" aria-label="回到首頁">
      <img src="/lavie-logo.svg" alt="La Vie" class="logo">
    </NuxtLink>

    <span class="search">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24" fill="currentColor">
        <g>
          <path fill="none" d="M0 0h24v24H0z"></path>
          <path
            d="M18.031 16.617l4.283 4.282-1.415 1.415-4.282-4.283A8.96 8.96 0 0 1 11 20c-4.968 0-9-4.032-9-9s4.032-9 9-9 9 4.032 9 9a8.96 8.96 0 0 1-1.969 5.617zm-2.006-.742A6.977 6.977 0 0 0 18 11c0-3.868-3.133-7-7-7-3.868 0-7 3.132-7 7 0 3.867 3.132 7 7 7a6.977 6.977 0 0 0 4.875-1.975l.15-.15z">
          </path>
        </g>
      </svg>
    </span>

  </div>

  <div class="label">

    <p>建築</p>
    <p>設計</p>
    <p>時尚</p>
    <p>生活</p>
    <p>藝術</p>
    <p>旅行</p>
    <p>美食</p>
    <p>展演</p>
    <p>雜誌出版</p>
    <p>特別企劃</p>
    <p>風格提案</p>

  </div>

  <div class="breadcrumb-end">

    <div class="breadcrumb">

      <nav aria-label="breadcrumb">
        <ol class="breadcrumb">
          <li class="breadcrumb-item"><a href="/">首頁</a></li>
          <li class="breadcrumb-item"><a href="/category">設計</a></li>
        </ol>
      </nav>

    </div>

  </div>

  <main class="page-all">
    <div class="page-left">
      <slot />
    </div>

    <aside class="page-right">
      <HotArticles />
    </aside>
  </main>

</template>
