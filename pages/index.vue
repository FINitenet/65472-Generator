<template>
  <v-stack class="m-8">
    <div class="chinese-font text-6xl">
      陆伍肆柒贰
    </div>
    <div class="chinese-font text-6xl">
      生成器
    </div>
    <br/>

    <v-stack>
      <v-stack v-if="isNoBGMode">
        <h-stack class="mb-1">
          <div class="font-bold md:text-5xl text-4xl text-red-600">
            <div v-if="poem.first.length>0" class="md:m-1 m-0.5">
              {{ poem.first }}
            </div>
            <div v-else class="md:m-1 m-0.5">&nbsp;</div>
          </div>
          <spacer/>
        </h-stack>
        <h-stack class="mb-1">
          <div class="font-bold md:text-5xl text-4xl text-blue-800">
            <div v-if="poem.second.length > 0" class="md:m-1 m-0.5">
              {{ poem.second }}
            </div>
            <div v-else class="md:m-1 m-0.5">&nbsp;</div>
          </div>
          <spacer/>
        </h-stack>
        <h-stack class="mb-1">
          <div class="font-bold md:text-5xl text-4xl text-red-600">
            <div v-if="poem.third.length>0" class="md:m-1 m-0.5">
              {{ poem.third }}
            </div>
            <div v-else class="md:m-1 m-0.5">&nbsp;</div>
          </div>
          <spacer/>
        </h-stack>
        <h-stack class="mb-1">
          <div class="font-bold md:text-5xl text-4xl text-blue-800">
            <div v-if="poem.fourth.length>0" class="md:m-1 m-0.5">
              {{ poem.fourth }}
            </div>
            <div v-else class="md:m-1 m-0.5">&nbsp;</div>
          </div>
          <spacer/>
        </h-stack>
        <h-stack class="mb-1">
          <div class="font-bold md:text-5xl text-4xl text-red-600">
            <div v-if="poem.fifth.length>0" class="md:m-1 m-0.5">
              {{ poem.fifth }}
            </div>
            <div v-else class="md:m-1 m-0.5">&nbsp;</div>
          </div>
          <spacer/>
        </h-stack>
        <h-stack v-if="poem.author.length>0" class="mb-1">
          <div class="font-bold text-md text-gray-700">
            <div class="md:m-1 m-0.5">
              @{{ poem.author }}
            </div>
          </div>
          <spacer/>
        </h-stack>
      </v-stack>

      <v-stack v-if="!isNoBGMode">
        <h-stack class="mb-1">
          <div class="font-bold md:text-5xl text-4xl text-white bg-red-600">
            <div v-if="poem.first.length>0" class="md:m-1 m-0.5">
              {{ poem.first }}
            </div>
            <div v-else class="md:m-1 m-0.5">&nbsp;</div>
          </div>
          <spacer/>
        </h-stack>
        <h-stack class="mb-1">
          <div class="font-bold md:text-5xl text-4xl text-white bg-blue-800">
            <div v-if="poem.second.length>0" class="md:m-1 m-0.5">
              {{ poem.second }}
            </div>
            <div v-else class="md:m-1 m-0.5">&nbsp;</div>
          </div>
          <spacer/>
        </h-stack>
        <h-stack class="mb-1">
          <div class="font-bold md:text-5xl text-4xl text-white bg-red-600">
            <div v-if="poem.third.length>0" class="md:m-1 m-0.5">
              {{ poem.third }}
            </div>
            <div v-else class="md:m-1 m-0.5">&nbsp;</div>
          </div>
          <spacer/>
        </h-stack>
        <h-stack class="mb-1">
          <div class="font-bold md:text-5xl text-4xl text-white bg-blue-800">
            <div v-if="poem.fourth.length>0" class="md:m-1 m-0.5">
              {{ poem.fourth }}
            </div>
            <div v-else class="md:m-1 m-0.5">&nbsp;</div>
          </div>
          <spacer/>
        </h-stack>
        <h-stack class="mb-1">
          <div class="font-bold md:text-5xl text-4xl text-white bg-red-600">
            <div v-if="poem.fifth.length>0" class="md:m-1 m-0.5">
              {{ poem.fifth }}
            </div>
            <div v-else class="md:m-1 m-0.5">&nbsp;</div>
          </div>
          <spacer/>
        </h-stack>
        <h-stack v-if="poem.author.length>0" class="mb-1">
          <div class="font-bold text-md text-gray-700">
            <div class="md:m-1 m-0.5">
              @{{ poem.author }}
            </div>
          </div>
          <spacer/>
        </h-stack>
      </v-stack>

      <div class="mt-4">
        <label
          for="toogle"
          class="flex items-center cursor-pointer"
        >
          <div class="relative">
            <input id="toogle" type="checkbox" v-model="isNoBGMode" class="sr-only" />
            <div class="w-10 h-5 bg-gray-200 rounded-full shadow-inner"></div>
            <div class="dot absolute w-6 h-6 bg-white rounded-full shadow -left-1 -top-1 transition"></div>
          </div>
          <div class="chinese-font mx-2">切换样式</div>
        </label>

      </div>

      <br/>
      <v-stack>
        <h-stack class="mx-1">
          <div class="chinese-font text-lg">第一行</div>
          <spacer/>
          <div class="chinese-font text-lg">{{ poem.first.length }} / 6</div>
        </h-stack>
        <input v-model="poem.first" class="border border-black text-gray-900 rounded-full block w-full p-4"/>
        <br/>
        <h-stack class="mx-1">
          <div class="chinese-font text-lg">第二行</div>
          <spacer/>
          <div class="chinese-font text-lg">{{ poem.second.length }} / 5</div>
        </h-stack>
        <input v-model="poem.second" class="border border-black text-gray-900 rounded-full block w-full p-4"/>
        <br/>
        <h-stack class="mx-1">
          <div class="chinese-font text-lg">第三行</div>
          <spacer/>
          <div class="chinese-font text-lg">{{ poem.third.length }} / 4</div>
        </h-stack>
        <input v-model="poem.third" class="border border-black text-gray-900 rounded-full block w-full p-4"/>
        <br/>
        <h-stack class="mx-1">
          <div class="chinese-font text-lg">第四行</div>
          <spacer/>
          <div class="chinese-font text-lg">{{ poem.fourth.length }} / 7</div>
        </h-stack>
        <input v-model="poem.fourth" class="border border-black text-gray-900 rounded-full block w-full p-4"/>
        <br/>
        <h-stack class="mx-1">
          <div class="chinese-font text-lg">第五行</div>
          <spacer/>
          <div class="chinese-font text-lg">{{ poem.fifth.length }} / 2</div>
        </h-stack>
        <input v-model="poem.fifth" class="border border-black text-gray-900 rounded-full block w-full p-4"/>
      </v-stack>
      <br/>
      <h-stack class="mx-1">
        <div class="chinese-font text-lg">诗人或许想留下姓名</div>
        <spacer/>
        <div class="chinese-font text-lg">（可选的题名处）</div>
      </h-stack>
      <input v-model="poem.author" class="border border-black text-gray-900 rounded-full block w-full p-4"/>

    </v-stack>

    <br/>
    <hr/>
    <br/>
    <div class="chinese-font text-lg">
      从统计学的角度来看，这个世界是需要诗歌的。
    </div>
    <br/>
    <div class="chinese-font text-lg">
      提起诗人，我们总是产生“感性”的印象，仿佛终日高谈歌咏无他事。
    </div>
    <div class="chinese-font text-lg">
      理性的诗人不这样，他们以戴着镣铐跳舞为乐。
    </div>
    <div class="chinese-font text-lg">
      要把自己塞进诸如五言、七言、五七五、十四行之类的桎梏中去。
    </div>
    <br/>
    <div class="chinese-font text-lg">
      最近，有一种红蓝相间、错落有致的新诗。
    </div>
    <div class="chinese-font text-lg">
      让感情在既定的结构里，最大限度地喷涌而出。
    </div>
    <br/>
    <div class="chinese-font text-lg">
      在上方作诗，然后截图分享给你的读者。
    </div>
    <div class="chinese-font text-lg">
      我想和你一起在风雨中吟咏，然后在或许马上就要到来、或许在很久之后才会到来的阳光下——
    </div>
    <br/>
    <div class="chinese-font text-lg">
      相遇。
    </div>

    <br/>

    <v-stack>
    <a href="https://github.com/TakiVotoid/65472-Generator"> <div class="italic">Github Link</div></a>
    </v-stack>
  </v-stack>
</template>

<script>
import HStack from "../components/utilities/layout/HStack";
import CustomInput from "../components/utilities/CustomInput";
import Stack from "../components/utilities/layout/Stack";
import VStack from "../components/utilities/layout/VStack";
import Spacer from "../components/utilities/layout/Spacer";

export default {
  components: {Spacer, VStack, Stack, CustomInput, HStack},
  data() {
    return {
      isNoBGMode: false,
      poem: {
        first: "我会做梦的吧",
        second: "在这个夜里，",
        third: "黎明将至，",
        fourth: "在城市边缘与你",
        fifth: "相遇",
        author: ""
      }
    }
  }
}
</script>

<style>
input:checked ~ .dot {
  transform: translateX(100%);
  background-color: #ffffff;
}
</style>
