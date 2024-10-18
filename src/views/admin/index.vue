<template>
        <div class="gvb_admin">
                <aside>
                        <div class="gvb_logo">
                             <img src="https://times-abema.ismcdn.jp/mwimgs/5/6/1448w/img_565e1a55d02d4a735e02547ac1acf4dd746018.jpg" alt="da">
                                <div style="font-size:22px;margin-left:20px;">
                                        bramble
                                 </div>
                        </div>
                        <a-menu
      :style="{ width: '200px', height: '100%' }"
      :default-open-keys="['0']"
      :default-selected-keys="['0_2']"
      show-collapse-button
      breakpoint="xl"
    >
      <a-sub-menu key="0">
        <template #icon><icon-apps></icon-apps></template>
        <template #title>Navigation 1</template>
        <a-menu-item key="0_0">Menu 1</a-menu-item>
        <a-menu-item key="0_1">Menu 2</a-menu-item>
        <a-menu-item key="0_2">Menu 3</a-menu-item>
        <a-menu-item key="0_3">Menu 4</a-menu-item>
      </a-sub-menu>
      <a-sub-menu key="1">
        <template #icon><icon-bug></icon-bug></template>
        <template #title>Navigation 2</template>
        <a-menu-item key="1_0">Menu 1</a-menu-item>
        <a-menu-item key="1_1">Menu 2</a-menu-item>
        <a-menu-item key="1_2">Menu 3</a-menu-item>
      </a-sub-menu>
      <a-sub-menu key="2">
        <template #icon><icon-bulb></icon-bulb></template>
        <template #title>Navigation 3</template>
        <a-menu-item key="2_0">Menu 1</a-menu-item>
        <a-menu-item key="2_1">Menu 2</a-menu-item>
        <a-sub-menu key="2_2" title="Navigation 4">
          <a-menu-item key="2_2_0">Menu 1</a-menu-item>
          <a-menu-item key="2_2_1">Menu 2</a-menu-item>
        </a-sub-menu>
      </a-sub-menu>
                        </a-menu>
                </aside>
                <main>
                        <div class="gvb_head">
                                <div class="gvb_bread_crumbs">
                                        <a-breadcrumb>
                                         <a-breadcrumb-item>Home</a-breadcrumb-item>
                                        <a-breadcrumb-item>Channel</a-breadcrumb-item>
                                        <a-breadcrumb-item>News</a-breadcrumb-item>
                                        </a-breadcrumb>
                                </div>
                                <div class="gvb_function_area">
                                        <icon-menu :style="{ margin: '10px 15px 10px 15px' }"></icon-menu>
                                        <div class="gvb_user_info_menu">
                                                <a-dropdown>
      <div style="display: flex; align-items: center; justify-content: center;">
        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTPSMsOf0WN_PQttn2O-8kMif2L4pv7aGkcZg&s" alt="da">
      <span style="margin-left: 10px;">bramble</span>
      </div>
      <template #content>
        <a-doption>Option 1</a-doption>
        <a-doption disabled>Option 2</a-doption>
        <a-doption>Option 3</a-doption>
        <a-doption>Option 4</a-doption>
        <a-doption>Option 5</a-doption>
        <a-doption>Option 6</a-doption>
      </template>
                                                 </a-dropdown>
                                        </div>
                                </div>
                        </div>
                        <div class="gvb_tabs">
                                <span class="gvb_tab active">首页</span>
                                <span class="gvb_tab">用户列表</span>
                                <span class="gvb_tab">文章列表</span>
                        </div>
                        <div class="gvb_container">
                                <router-view/>da
                        </div>
                右下内容
                </main>
        </div>
        

</template>
<script setup lang="ts">

import {
 IconDown,
  IconMenu,
  IconMenuFold,
  IconMenuUnfold,
  IconApps,
  IconBug,
  IconBulb,
} from '@arco-design/web-vue/es/icon';

</script>

<style lang="scss">
.gvb_admin{
        display: flex;
        aside{
                width: 240px;
                border-right: 8px solid var(--bg);
                height: 100vh;
                .gvb_logo{
                        height: 90px;
                        display: flex;
                        padding: 20px;
                        align-items: center;
                        border-bottom: 8px solid var(--bg);
                        img{
                        width: 60px;
                        height: 60px;
                         }
                }
        }
        main{
                width: calc(100% - 240px);

                .gvb_head{
                        width: 100%;
                        height: 60px;
                        border-bottom: 5px solid var(--bg);
                        display: flex;
                        justify-content: space-between;
                        padding: 20px 20px;
                        align-items: center;
                        .gvb_function_area{
                                display: flex;
                                align-items: center;
                                .gvb_user_info_menu{
                                        img{
                                                width: 30px;
                                                height: 30px;
                                                border-radius: 50%;
                                        }
                                }
                        }
                }
                .gvb_tabs{
                        height: 30px;
                        width: 100%;
                        border-bottom: 8px solid var(--bg);
                        padding: 0 20px;
                        display: flex;
                        align-items: center;
                        .gvb_tab{
                                border-radius: 5px;
                                border-bottom: 1px solid var(--bg);
                                padding: 3px;
                                margin-right: 10px;
                                cursor: pointer;
                        }
                        .gvb_tab.active { /* 修改这一行 */
                        background-color: rgb(178, 120, 231);
                        color: white;
                        border: none;
}
                }
                .gvb_container{
                        // background-color: rgb(9, 95, 171);
                        min-height: calc(100vh - 90px);
                        padding: 20px;
                }

        }
}

</style>