# Chrome Devtools Performance

<div class="flex gap-32 mt-10">
  <div class="flex flex-col gap-16">
  <v-clicks> 
  <div class="flex flex-col gap-2">
      <span class="text-zinc-500 text-base">Это там наверху где-то </span>
      <img class="w-90" src="/tabs.png" />
    </div>
    <div class="flex flex-col gap-2">
      <span class="text-zinc-500 text-base">Здесь уже можно произвести запись</span>
      <img class="w-90" src="/performance.png" />
    </div>
  </v-clicks>
  </div>
  <div>
  <v-clicks> 
 <div class="flex flex-col gap-4 mt-1">
      <span class="text-zinc-500 text-base">Без KeepAlive: </span>
      <img class="w-60" src="/chrome_none.png" />
    </div>
    <div class="flex flex-col mt-10 gap-4">
      <span class="text-zinc-500 text-base">С KeepAlive: </span>
      <img class="w-60" src="/chrome.png" />
    </div>
  </v-clicks>
  </div>
</div>

<!-- Обратимся к такой замечательной штуке как Chrome Devtools и табу performace
Измерения проводились в течении 40 секунд (вводили данные и переключались между страницами)
Scripting (Время скриптов): Время, потраченное на выполнение JavaScript.
Rendering (Время рендеринга): Время, потраченное на отрисовку компонентов в браузере.

KeepAlive сохраняет состояние компонентов и предотвращает необходимость повторного выполнения некоторых скриптов при переключении между компонентами.
KeepAlive позволяет избежать повторной полной отрисовки при повторной активации компонентов.
 -->
