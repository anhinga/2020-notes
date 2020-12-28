# Dataflow matrix machines по-русски

Меня попросили написать очень неформальный текст про dataflow matrix machines по-русски, по-возможности, простой и не очень длинный.

I was asked to write a short very informal note on dataflow matrix machines in Russian.

## Мотивировка

Когда я учился в институте в Москве в первой половине 80-х годов, меня очень достала необходимость всё время программировать, и я заинтересовался задачами автоматизации этого процесса. Довольно быстро стало ясно, что одним из главных препятствий к автоматическому синтезу программ является дискретность типичного пространства программ и большая чувствительность программ к изменению, вообще говоря, даже одной буквы. До сих пор, успехи в автоматическом синтезе программ крайне скромные, именно из-за этого обстоятельства.

Меж тем, прикладные математики имеют большой опыт в синтезе разнообразных непрерывных объектов на компьютере - синтез кривых (функций и их графиков), поверхностей, матриц коэффициентов связей искусственных нейронных сетей - все эти задачи гораздо легче решаются на компьютере, чем задачи синтеза дискретных объектов.

Отсюда возникла задача - понять, каким образом можно программировать так, чтобы **программы можно было деформировать непрерывным образом** (чтобы **программы допускали сколь угодно малое изменение**). Вот, этой задачей я пробую заниматься с тех пор с разных углов, но удовлетворительное решение нашлось только в районе 2015-го года.

## Решение

Довольно долго я занимался непрерывными моделями обычных программ и пробовал извлечь из этих занятий способы "непрерывной в некотором смысле деформации обычных программ", но это оказался, по-видимому, довольно тупиковый путь. Правильным решением оказалось придумать некоторый специализированный новый формализм программирования, достаточно богатый и выразительный, чтобы на нём было можно с удобством программировать всё, что может захотеться программировать, но который, при этом, допускал бы непрерывные деформации программ.

Оказалось, что надо думать в терминах потоков данных, которые можно комбинировать друг с другом с коэффициентами (скажем половина такого потока, и треть другого, и одна шестая третьего). И вот, нужно программировать в терминах комбинаций этих потоков с коэффициентами, и соединения преобразователей этих потоков в сети (**нечто вроде искусственных нейронных сетей, но только вместо потоков чисел мы работаем с потоками более сложных объектов**).

Например, можно рассмотреть **потоки картинок (то есть, анимации)**. Вот видео одного из моих первых генераторов анимаций, которые я запрограммировал в этом стиле в 2015 году:

[анимация, запрограммированная в стиле dataflow](https://youtu.be/fEWcg_A5UZc)

Картинки можно смешивать с коэффициэнтами. На этом 30-секудном видео половина анимации в левом нижнем квадрате смешивается с половиной анимации в левом вернем квадрате, давая анимацию, показываемую в правом нижнем квадрате. В последние несколько секунд видео мы начинаем интерактивно менять эти коэффициенты, на 23-ей секунде сначала плавно увеличивая долю левого верхнего квадрата и уменьшая долю левого нижнего, затем наоборот.

Смешивание разных видео с коэффициентами - идея не новая, видео-жокеи давно это делают, когда смешивают разные видео вместе во время своих представлений:

https://en.wikipedia.org/wiki/VJing

Новым здесь является осознание того, что программирование в таком стиле достаточно выразительно, чтобы и вообще программировать таким образом более-менее какие угодно программистские задачи (к 2020-му году мы набрали довольно большую коллекцию программистских упражнений, выполненных в этом стиле).

Единственный нюанс состоит в том, чтобы чередовать произвольные, возможно нелинейные преобразования таких потоков и комбинации этих потоков с коэффициентами (такие комбинации с коэффициентами мы называем линейными комбинациями; таким образом **чередуются произвольные преобразования потоков и линейные**; если мы это делаем, то мы можем плавно менять коэффициенты в линейных преобразованиях, и оказывается, что таким образом **можно плавно преобразовать любую программу в любую другую**).

## Публикации и развитие

Первая статья на эту тему была нами опубликована в 2015-ом году: [Linear Models of Computations and Program Learning](https://easychair.org/publications/paper/Q4lW)

Дальше было изучение и развитие этого формализма, разные доклады на конференциях и open source software implementations. Среди прочего, в процессе этих исследований стало понятно, как сделать так, чтобы **эти нейронные машины могли менять сами себя сколь угодно гибкими способами**.

Каноническая статья на эту тему была опубликована в 2017-ом году: [Dataflow Matrix Machines and V-values: a Bridge between Programs and Neural Nets](https://arxiv.org/abs/1712.07447)

Тогда же я записал 15-минутный доклад на видео:https://youtu.be/X6GCohQ-LHM

В 2018-ом году появились слайды с красивыми картинками: https://researcher.watson.ibm.com/researcher/files/us-lmandel/aisys18-bukatin.pdf

В 2019-ом году появилась красивая "карта местности": https://anhinga.github.io/

Недавно появилась программа интердисциплинарных исследований, связанных с этим материалом, которые было бы интересно сделать в сотрудничестве: https://www.cs.brandeis.edu/~bukatin/dmm-collaborative-research-agenda.pdf

В частности, недавно мы осознали, что есть глубокие связи между тем, что мы делаем, и новыми популярными классами моделей, основанных на искусственном внимании (**"attention-based models"**, в частности, связи между нашими моделями и новыми сверх-популярные моделями, которые называются **Transformers**, которые изобрели в 2017-ом году и которые произвели супер-сенсацию в этом году), и я в последние месяцы всё больше смотрю на эти связи.

Это всё было сделано в небольших коллаборациях в два-три человека; последнее время я, вообще, занимаюсь этим в одиночку и ищу новые коллаборации.


## Почему это было открыто так поздно, и когда этим начнут пользоваться?