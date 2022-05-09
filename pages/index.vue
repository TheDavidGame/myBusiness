<template>
  <div class="body">
    <header class="header">
      <div class="wrapper">
        <div class="header__wrapper">
          <nav class="header__nav">
            <ul class="header__list">
              <li class="header__item">
                <button
                  class="text-white not-italic text-base font-Circe bg-[#FE5F5F] hover:bg-rose-600 px-8 py-2 rounded-full"
                >
                  Личный кабинет
                </button>
              </li>
              <li class="header__item">
                <a href="#!" class="header__link">Каталог услуг </a>
              </li>
            </ul>
          </nav>
          <div class="header__list-onlineHelp">
            <img
              src="../static/online__help.svg"
              alt="myBusiness"
              class="header__pic"
            />
            <a href="#!" class="header__onlineHelp">Онлайн помощник</a>
          </div>
        </div>
        <div class="bottomHeader">
          <div class="bottomHeader__wrapper">
            <section class="logo">
              <div class="logo__wrapper">
                <img
                  src="../static/logo.svg"
                  alt="logoMyBusiness"
                  class="logo__pic"
                />
              </div>
            </section>
            <section class="intro">
              <div class="intro__wrapper">
                <h1 class="intro__title">
                  Мой бизнес - цифровая платформа для тех, кто хочет открыть и
                  развивать свой бизнес
                </h1>
              </div>
            </section>
          </div>
        </div>
      </div>
    </header>
    <div class="underHeader">
      <div class="underHeader__wrapper">
        <div class="underHeader__wrapper-list">
          <div class="underHeader__title">
            Для начала работы ответьте на вопрос, есть ли у вас уже существующий
            бизнес?
          </div>
          <nav class="underHeader__nav">
            <ul class="underHeader__list">
              <li class="underHeader__item">
                <button
                  class="text-white not-italic text-base font-Circe bg-[#FE5F5F] hover:bg-rose-600 px-14 py-3 rounded-full"
                >
                  Да, у меня уже есть бизнес
                </button>
              </li>
              <li class="underHeader__item">
                <button
                  class="text-white not-italic text-base font-Circe bg-[#3865A7] hover:bg-[#1d4175] px-14 py-3 rounded-full"
                >
                  Нет, но планирую открыть
                </button>
              </li>
            </ul>
          </nav>
        </div>
      </div>
    </div>
    <main class="main">
      <div class="main__wrapper">
        <div class="main__wrapper-title">
          <img class="main__point" src="../static/point.svg" alt="pointStart" />
          <div class="main__title">Преимущества</div>
          <img class="main__point" src="../static/point.svg" alt="pointEnd" />
        </div>
        <div class="main__wrapper-list">
          <nav class="main__nav">
            <ul class="main__list grid grid-cols-3 gap-4">
              <mainItems
                v-for="(item, i) in mainItem"
                :key="i"
                class="main__item"
                :pic="item.pic"
                :text="item.text"
                :number="item.number"
              >
              </mainItems>
            </ul>
          </nav>
        </div>
      </div>
      <div class="main__underWrapper">
        <div class="main__underWrapper-title">
          <img class="main__point" src="../static/point.svg" alt="pointStart" />
          <div class="main__underTitle">Истории успеха</div>
          <img class="main__point" src="../static/point.svg" alt="pointStart" />
        </div>
        <div class="main__underWrapper-list">
          <nav class="main__underNav">
            <ul class="main__underList">
              <mainUnderItem
                v-for="(item, i) in mainUnderItem"
                :key="i"
                class="main__underItem"
                :pic="item.pic"
                :title="item.title"
                :subTitle="item.subTitle"
                :text="item.text"
              >
              </mainUnderItem>
            </ul>
          </nav>
        </div>
      </div>
    </main>
    <footer class="footer">
      <div class="footertop">
        <div class="footertop__wrapper">
          <div class="footertop__wrapper-list">
            <div class="footertop__title">Есть вопросы?</div>
            <div class="footertop__subtitle">
              Задайте интересующие вас вопросы онлайн помощнику
            </div>

            <button
              class="bg-[#FE5F5F] hover:bg-rose-600 px-12 py-2 rounded-full"
            >
              <div class="footertop__button">
                <img
                  src="../static/rocket.svg"
                  alt="rocket"
                  class="footertop__pic"
                />
                <div class="footertop_button-text">Онлайн помощник</div>
              </div>
            </button>
          </div>
        </div>
      </div>
      <div class="footerbottom">
        <div class="footerbottom-wrapper">
          <div class="footerbottom__wrapper-list">
            <nav class="footerbottom__nav">
              <ul class="footerbottom__list">
                <li class="footerbottom__item">
                  <a href="#!" class="footerbottom__link"
                    >Услуги и поддержка
                  </a>
                </li>
                <li class="footerbottom__item">
                  <a href="#!" class="footerbottom__link"
                    >Сервисы для бизнеса
                  </a>
                </li>
                <li class="footerbottom__item">
                  <a href="#!" class="footerbottom__link">Общая информация </a>
                </li>
                <li class="footerbottom__item">
                  <a href="#!" class="footerbottom__link">Защита бизнеса </a>
                </li>
                <li class="footerbottom__item">
                  <a href="#!" class="footerbottom__link"
                    >service@in-line.ru
                  </a>
                </li>
                <li class="footerbottom__item">
                  <a href="#!" class="footerbottom__link"> 8-800-200-74-30 </a>
                </li>
              </ul>
            </nav>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      mainItem: [
        {
          pic: 'item1',
          number: 482,
          text: 'Организаций поддержки по Российской Федерации',
        },
        {
          pic: 'item2',
          number: 5240,
          text: 'Оказано услуг государственной поддержки',
        },
        {
          pic: 'item3',
          number: 1360,
          text: 'Зарегестрировано участников проекта',
        },
      ],
      mainUnderItem: [
        {
          pic: 'item1',
          title: 'Пекарня “Русские традиции”',
          subTitle:
            'Как говорит сам Владимир: «мне хотелось, чтобы все узнали, что такое русская кухня», «обьяснить, что она жива».',
          text: 'Чтобы мини-пекарня стала рентабельным бизнесом, необходимы строгие расчеты, учет рисков и перспектив, анализ рынка, налаживание сбыта.',
        },
        {
          pic: 'item2',
          title: 'Автомастерская',
          subTitle:
            'Первые дни независимости. Когда не нужно рано вставать, когда не нужно отпрашиваться, что бы успеть съездить в магазин, когда удобно.',
          text: 'Встреча в городе Н с моими будущими партнерами была плодотворной. Я не смог заснуть до пяти утра – не потому что не спалось, но потому что мысли о будущих перспективах просто взрывали мой мозг. ',
        },
        {
          pic: 'item3',
          title: 'Салон красоты “Эмират”',
          subTitle:
            'Когда же появилась возможность открыть свой бизнес, я рассматривала различные варианты, изучала всевозможные направления.',
          text: '',
        },
      ],
    }
  },
}
</script>

<style>
.body {
  font-family: 'Circe';
  font-style: normal;
}

.wrapper {
  height: 900px;
  background: url(../static/background_main.svg) no-repeat center;
  background-size: cover;
}
@media (max-width: 600px) {
  .wrapper {
    width: 100vh;
  }
}

/* Header styles start */
.header__wrapper {
  max-width: 1111px;
  margin: 0 auto;
  padding-top: 42px;
  display: flex;
  flex-wrap: wrap;
  align-items: flex-end;
  justify-content: space-between;
}

.header__list {
  display: flex;
  flex-wrap: wrap;
}
.header__list-onlineHelp {
  display: flex;
  flex-wrap: wrap;
}
.header__onlineHelp {
  margin-left: 15px;
  color: #fe5f5f;
  font-weight: 700;
  font-size: 16px;
  line-height: 122.4%;
  padding-top: 10px;
}
.header__item {
  margin-right: 27.5px;
}
.header__link {
  font-size: 16px;
  line-height: 40px;
  text-decoration: none;
}
.header__link:hover,
.header__link:focus,
.header__link:active {
  opacity: 0.75;
}
.header__onlineHelp:hover,
.header__onlineHelp:focus,
.header__onlineHelp:active {
  opacity: 0.75;
}
/* Header styles end */

/* UnderHeader styles start */
.bottomHeader__wrapper {
  max-width: 1111px;
  margin: 0 auto;
}
.logo {
  padding-top: 63px;
}
.intro {
  padding-top: 63px;
}
.intro__wrapper {
  max-width: 576px;
}
.intro__title {
  font-weight: 700;
  font-size: 35px;
  line-height: 111.4%;
  color: #2b2b2b;
}
.underHeader__wrapper {
  height: 320px;
  background: url(../static/underHeader.svg) no-repeat center;
  background-size: cover;
}
@media (max-width: 600px) {
  .underHeader__wrapper {
    width: 100vh;
  }
}
.underHeader__wrapper-list {
  max-width: 814px;
  margin: 0 auto;
  padding-top: 72px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.underHeader__title {
  text-indent: 0.4em;
  max-width: 552px;
  justify-content: center;
  font-weight: 700;
  font-size: 30px;
  line-height: 35px;
}
.underHeader__list {
  padding-top: 39px;
  display: flex;
  flex-direction: row;
  align-items: flex-center;
  justify-content: space-between;
}
.underHeader__item {
  margin-right: 26px;
}
.underHeader__item:last-child {
  margin-right: 0px;
}
/* UnderHeader styles end */

/* Main styles start */
.main__wrapper {
  padding-top: 159px;
  max-width: 919px;
  margin: 0 auto;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  flex-direction: column;
  justify-content: center;
}
@media (max-width: 600px) {
  .main__wrapper {
    width: 100vh;
  }
}
.main__wrapper-title {
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
}
.main__title {
  font-weight: 700;
  font-size: 40px;
  line-height: 122.4%;
}
.main__point {
  margin: 1em;
}
.main__wrapper-list {
  padding-top: 97px;
}
.main__underWrapper {
  padding-top: 240px;
  max-width: 1000px;
  margin: 0 auto;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  flex-direction: column;
  justify-content: center;
}
.main__underWrapper-title {
  width: 380px;
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
}
.main__underTitle {
  font-weight: 700;
  font-size: 40px;
  line-height: 122.4%;
}
/* Main styles end */

/* FooterTop styles start */
.footertop__wrapper {
  height: 320px;
  background: url(../static/footertop.svg) no-repeat center;
  background-size: cover;
}
@media (max-width: 600px) {
  .footertop__wrapper {
    width: 100vh;
  }
}
.footertop__wrapper-list {
  padding-top: 48px;
  max-width: 268px;
  margin: 0 auto;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  flex-direction: column;
  justify-content: center;
  text-align: center;
}
.footertop__title {
  padding-bottom: 7px;
  font-weight: 700;
  font-size: 35px;
  line-height: 52px;
}
.footertop__subtitle {
  padding-bottom: 29px;
  font-weight: 400;
  font-size: 16px;
  line-height: 24px;
}

.footertop__button {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
}
.footertop_button-text {
  font-size: 16px;
  line-height: 122.4%;
  padding-left: 9.88px;
  color: #ffffff;
}
/* FooterTop styles end */

/* FooterBottom styles start */
.footerbottom-wrapper {
  height: 86px;
  background: #2f2f2f;
}
@media (max-width: 600px) {
  .footerbottom-wrapper {
    width: 100vh;
  }
}
.footerbottom__wrapper-list {
  max-width: 1130px;
  margin: 0 auto;
  padding-top: 42px;
  display: flex;
  flex-wrap: wrap;
  align-items: flex-end;
  justify-content: space-between;
}
.footerbottom__list {
  display: flex;
  flex-wrap: wrap;
}
.footerbottom__item {
  margin-right: 44px;
}
.footerbottom__item:hover,
.footerbottom__item:focus,
.footerbottom__item:active {
  opacity: 0.75;
}
.footerbottom__item:nth-child(4) {
  margin-right: 126px;
}

.footerbottom__item:last-child {
  margin-right: 0px;
}
.footerbottom__link {
  font-size: 16px;
  line-height: 24px;
  letter-spacing: 0.01em;
  color: #ffffff;
}
/* FooterBottom styles end */
</style>
