# MutObsLib
Mutation Observer for Undo Redo

Инициализируем и запускаем менеджер повтора/отмены действий чтобы он 
следил за изменениями элемента по ID, если не передать то будет следить за body

    window.moUndoRedo = new undoredo.MutObs(document.getElementById("element"));

Остановить отслеживание

    moUndoRedo.disconnect();

Перезапуск отслеживания изменений 

    moUndoRedo.reObserve();

Очистка истории изменений

    moUndoRedo.reset();

Хранит историю изменений

    moUndoRedo.historyList


Повтор действия (входным параметром можно передать количество шагов повтора количество мутаций вперед)

    moUndoRedo.redo():


Отмена действия (входным параметром можно передать количество шагов отмены - количество мутаций назад)

    moUndoRedo.undo();