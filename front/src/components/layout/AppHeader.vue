<template>
  <!-- Header Section -->
  <header class="header" id="header">
    <nav class="navbar container">
      <a href="" class="brand"
        ><img src="/images/value/emblem_kr.svg" alt="" class="brand-logo" />
        <img src="/images/value/flag.png" alt="" class="brand-logo" />
        <p>
          <strong>{{ $t("City hall") }}</strong>
          {{ $t("Region") }}
        </p>
      </a>
      <input type="checkbox" name="" id="check" />
      <label class="burger" for="check"
        ><span class="burger-line"></span>
        <span class="burger-line"></span>
        <span class="burger-line"></span
      ></label>
      <input type="checkbox" name="" id="check2" />
      <label class="burger-decs" for="check2"
        ><span class="burger-line"></span>
        <span class="burger-line"></span>
        <span class="burger-line"></span
      ></label>

      <div class="menu" id="menu">
        <ul class="menu-inner">
          <li v-for="item in menus" :key="item.title"  :class="['menu-item', item.children !== null ? 'menu-link' : '']">
            <router-link v-if="item.children.length === 0" :to="{ path: item.link }" class="menu-link">{{ $t(item.title) }}</router-link>
            <a v-else>
              <span>{{ $t(item.title) }} </span>
              <ul class="menu-link-list">
                <li v-for="sub in item.children" :key="sub.title">
                  <router-link :to="{ path: sub.link }" class="menu-link">{{ $t(sub.title) }}</router-link>
                </li>
              </ul>
            </a>
          </li>
<!--          <li class="menu-item">
            <router-link to="/" class="menu-link">{{ $t("Home") }}</router-link>
          </li>
          <li class="menu-item">
            <router-link to="/news" class="menu-link">{{
              $t("News")
            }}</router-link>
          </li>
          <li class="menu-item">
            <router-link to="/opendata" class="menu-link">{{
              $t("Open Data")
            }}</router-link>
          </li>
          <li class="menu-item">
            <router-link to="/documents" class="menu-link">{{
              $t("Documents")
            }}</router-link>
          </li>
          <li class="menu-item menu-link">
            <a>
              <span>{{ $t("Area") }} </span>
              <ul class="menu-link-list">
                <li>
                  <router-link to="/area" class="menu-link">{{
                    $t("About")
                  }}</router-link>
                </li>
                <li>
                  <router-link to="/management" class="menu-link">{{
                    $t("General Information")
                  }}</router-link>
                </li>
                <li>
                  <router-link to="/deputies" class="menu-link">{{
                    $t("Peoples deputies")
                  }}</router-link>
                </li>
              </ul>
            </a>
          </li>
          <li class="menu-item">
            <router-link to="/feedback" class="menu-link">{{
              $t("Feedback")
            }}</router-link>
          </li>
          <li class="menu-item">
            <router-link to="/more" class="menu-link">{{
              $t("Fighting Corruption")
            }}</router-link>
          </li>-->
          <ul class="social-lang">
            <li><a @click="uzLang">??????</a></li>
              <li><a @click="kkLang">????</a></li>
              <li><a @click="ruLang">??????</a></li>
              <li><a @click="enLang">Eng</a></li>
          </ul>
          <ul class="social-list">
            <li>
              <a
                target="_blank"
                href="https://t.me/shmirziyoyev"
                title="Telegram"
              >
                <span>
                  <img src="/images/social/telegram.png" alt="" />
                </span>
                Telegram
              </a>
            </li>
            <li>
              <a
                target="_blank"
                href="https://www.facebook.com/Mirziyoyev/?ref=ts&amp;fref=ts"
                title="Facebook"
              >
                <span>
                  <img src="/images/social/facebook.png" alt="" />
                </span>
                Facebook
              </a>
            </li>
            <li>
              <a
                target="_blank"
                href="https://www.instagram.com/mirziyoyev_sh/"
                title="Instagram"
              >
                <span>
                  <img src="/images/social/instagram.png" alt="" />
                </span>
                Instagram
              </a>
            </li>
            <li>
              <a
                target="_blank"
                href="https://twitter.com/president_uz"
                title="Twitter"
              >
                <span>
                  <img src="/images/social/twiter.png" alt="" />
                </span>
                Twitter
              </a>
            </li>
            <li>
              <a
                target="_blank"
                href="https://www.youtube.com/channel/UC61Jnumjuz8NXhSuLoZD2xg"
                title="Youtube"
              >
                <span>
                  <img src="/images/social/youtube.png" alt="" />
                </span>
                Youtube
              </a>
            </li>
          </ul>
        </ul>
      </div>
      <div class="social" id="menu">
        <ul class="social-inner">
          <div class="social-header">
            <ul class="social-lang">
              <li><a @click="uzLang">??????</a></li>
              <li><a @click="kkLang">????</a></li>
              <li><a @click="ruLang">??????</a></li>
              <li><a @click="enLang">Eng</a></li>
            </ul>
            <!-- <p> -->
            <br />

            <!-- </p> -->
            <ul class="social-list">
              <li>
                <a
                  target="_blank"
                  href="https://t.me/hokimgamurojaat"
                  title="Telegram"
                >
                  <span>
                    <img src="/images/social/telegram.png" alt="" />
                  </span>
                  Telegram
                </a>
              </li>
              <li>
                <a
                  target="_blank"
                  href="https://www.facebook.com/profile.php?id=100079487263413"
                  title="Facebook"
                >
                  <span>
                    <img src="/images/social/facebook.png" alt="" />
                  </span>
                  Facebook
                </a>
              </li>
              <li>
                <a
                  target="_blank"
                  href="https://www.instagram.com/xojelirk.uz/"
                  title="Instagram"
                >
                  <span>
                    <img src="/images/social/instagram.png" alt="" />
                  </span>
                  Instagram
                </a>
              </li>
<!--              <li>
                <a
                  target="_blank"
                  href="https://twitter.com/president_uz"
                  title="Twitter"
                >
                  <span>
                    <img src="/images/social/twiter.png" alt="" />
                  </span>
                  Twitter
                </a>
              </li>-->
              <li>
                <a
                  target="_blank"
                  href="https://youtube.com/channel/UCntUKeshWwVn8G4j3WEHw2w"
                  title="Youtube"
                >
                  <span>
                    <img src="/images/social/youtube.png" alt="" />
                  </span>
                  Youtube
                </a>
              </li>
            </ul>
          </div>
        </ul>
      </div>
    </nav>
  </header>
</template>

<script setup>
import { reactive } from "vue";
import { useI18n } from "vue-i18n";
const { t, locale } = useI18n({ useScope: "global" });

const menus = reactive(
  [
    {
      title: "Home",
      link: "/",
      children: [],
    },
    {
      title: "News",
      link: "/news",
      children: [],
    },
    {
      title: "Open Data",
      link: "/opendata",
      children: [],
    },
    {
      title: "Documents",
      link: "/documents",
      children: [],
    },
    {
      title: "Area",
      link: "about",
      children: [
        {
          title: "About",
          link: "area",
        },
        {
          title: "General Information",
          link: "management",
        },
        {
          title: "Peoples deputies",
          link: "deputies",
        },
      ],
    },
    {
      title: "Feedback",
      link: "/feedback",
      children: [],
    },
    {
      title: "Fighting Corruption",
      link: "/anti-core",
      children: [],
    },
  ],
)

const uzLang = () => {
  locale.value = "uz";
  localStorage.setItem("lang", locale.value);
};
const enLang = () => {
  locale.value = "en";
  localStorage.setItem("lang", locale.value);
};
const ruLang = () => {
  locale.value = "ru";
  localStorage.setItem("lang", locale.value);
};
const kkLang = () => {
  locale.value = "kk";
  localStorage.setItem("lang", locale.value);
};
</script>