```php
use Illuminate\Database\Seeder;
use App\Models\Exercise;

class ExerciseSeeder extends Seeder
{
    /**
     * Run the database seeds.
     *
     * @return void
     */
    public function run()
    {
        $exercises = [
            [
                'name' => 'Sentadillas',
                'description' => 'Las sentadillas son un ejercicio compuesto que trabaja los músculos de las piernas y glúteos. Se realiza flexionando las rodillas y caderas mientras se mantiene la espalda recta.',
            ],
            [
                'name' => 'Peso muerto',
                'description' => 'El peso muerto es un ejercicio de levantamiento de peso que involucra principalmente los músculos de la espalda baja, glúteos y piernas. Se realiza levantando una barra desde el suelo hasta la posición de pie.',
            ],
            [
                'name' => 'Press de banca',
                'description' => 'El press de banca es un ejercicio de entrenamiento de fuerza que se enfoca en los músculos del pecho, tríceps y hombros. Se realiza acostado en un banco horizontal y empujando una barra hacia arriba y hacia abajo.',
            ],
            [
                'name' => 'Dominadas',
                'description' => 'Las dominadas son un ejercicio de entrenamiento de fuerza que se enfoca en los músculos de la espalda y los brazos. Se realiza colgándose de una barra y levantando el cuerpo hasta que la barbilla esté por encima de la barra.',
            ],
            [
                'name' => 'Fondos de tríceps',
                'description' => 'Los fondos de tríceps son un ejercicio de entrenamiento de fuerza que se enfoca en los músculos del tríceps. Se realiza apoyando las manos en una superficie elevada y bajando el cuerpo flexionando los codos.',
            ],
            [
                'name' => 'Remo con barra',
                'description' => 'El remo con barra es un ejercicio que trabaja los músculos de la espalda, los hombros y los brazos. Se realiza inclinándose hacia adelante con las rodillas ligeramente flexionadas y levantando una barra hacia el pecho.',
            ],
            [
                'name' => 'Press militar',
                'description' => 'El press militar es un ejercicio de entrenamiento de fuerza que se enfoca en los músculos de los hombros y tríceps. Se realiza de pie, levantando una barra desde los hombros hasta una posición extendida sobre la cabeza.',
            ],
            [
                'name' => 'Curl de bíceps',
                'description' => 'El curl de bíceps es un ejercicio de aislamiento que se enfoca en los músculos de los brazos. Se realiza levantando una barra o mancuernas desde la posición inicial con los brazos extendidos hasta la contracción del bíceps.',
            ],
            [
                'name' => 'Elevaciones laterales',
                'description' => 'Las elevaciones laterales son un ejercicio de aislamiento que se enfoca en los músculos de los hombros. Se realiza de pie

, levantando las pesas hacia los lados hasta que los brazos estén paralelos al suelo.',
            ],
            [
                'name' => 'Zancadas',
                'description' => 'Las zancadas son un ejercicio compuesto que trabaja los músculos de las piernas y glúteos. Se realiza dando un paso hacia adelante y flexionando ambas rodillas hasta que la rodilla trasera esté cerca del suelo.',
            ],
            [
                'name' => 'Crunch abdominal',
                'description' => 'El crunch abdominal es un ejercicio de entrenamiento de fuerza que se enfoca en los músculos abdominales. Se realiza acostado en el suelo con las rodillas flexionadas y levantando el torso hacia las rodillas.',
            ],
            [
                'name' => 'Flexiones de pecho',
                'description' => 'Las flexiones de pecho son un ejercicio de entrenamiento de fuerza que se enfoca en los músculos del pecho, hombros y tríceps. Se realiza apoyando las manos y los pies en el suelo y bajando el cuerpo hacia el suelo y luego empujándolo hacia arriba.',
            ],
            [
                'name' => 'Pájaros',
                'description' => 'Los pájaros son un ejercicio de aislamiento que se enfoca en los músculos de la espalda y los hombros. Se realiza de pie o inclinado hacia adelante, levantando pesas hacia los lados hasta que los brazos estén paralelos al suelo.',
            ],
            [
                'name' => 'Extensiones de tríceps',
                'description' => 'Las extensiones de tríceps son un ejercicio de aislamiento que se enfoca en los músculos del tríceps. Se realiza acostado o sentado, levantando una pesa o mancuerna sobre la cabeza y luego bajándola detrás de la cabeza flexionando los codos.',
            ],
            [
                'name' => 'Desplantes',
                'description' => 'Los desplantes son un ejercicio compuesto que trabaja los músculos de las piernas y glúteos. Se realiza dando un paso hacia adelante y flexionando ambas rodillas hasta que ambas estén dobladas en un ángulo de 90 grados.',
            ],
            [
                'name' => 'Patada de glúteos',
                'description' => 'La patada de glúteos es un ejercicio de aislamiento que se enfoca en los músculos de los glúteos. Se realiza a cuatro patas, extendiendo una pierna hacia atrás y hacia arriba mientras se mantiene el torso estable.',
            ],
            [
                'name' => 'Elevaciones de pantorrillas',
                'description' => 'Las elevaciones de pantorrillas son un ejercicio de aislamiento que se enfoca en los músculos de las pantorrillas. Se realiza de pie, levantando los talones mientras se mantiene el cuerpo estable.',
            ],
            [
                'name' => 'Prensa de piernas',
                'description' => 'La prensa de piernas es un ejercicio de entrenamiento de fuerza que se enfoca en los músculos de las piernas. Se realiza en una máquina de prensa, empujando el peso con los pies hacia afuera y luego

 volviendo a la posición inicial.',
            ],
            [
                'name' => 'Flexiones de tríceps',
                'description' => 'Las flexiones de tríceps son un ejercicio de entrenamiento de fuerza que se enfoca en los músculos del tríceps. Se realiza apoyando las manos en una superficie elevada y bajando el cuerpo flexionando los codos.',
            ],
            [
                'name' => 'Curl de martillo',
                'description' => 'El curl de martillo es un ejercicio de aislamiento que se enfoca en los músculos de los brazos. Se realiza levantando una pesa o mancuerna desde la posición inicial con los brazos extendidos, manteniendo los codos fijos y girando las muñecas hacia arriba.',
            ],
            [
                'name' => 'Elevaciones frontales',
                'description' => 'Las elevaciones frontales son un ejercicio de aislamiento que se enfoca en los músculos de los hombros. Se realiza de pie, levantando pesas desde el frente del cuerpo hasta que los brazos estén paralelos al suelo.',
            ],
            [
                'name' => 'Step-ups',
                'description' => 'Los step-ups son un ejercicio compuesto que trabaja los músculos de las piernas y glúteos. Se realiza subiendo y bajando de un step o plataforma con una pierna a la vez.',
            ],
            [
                'name' => 'Russian twist',
                'description' => 'El Russian twist es un ejercicio de entrenamiento de fuerza que se enfoca en los músculos abdominales y oblicuos. Se realiza sentado en el suelo con las piernas flexionadas, inclinando el torso hacia atrás y girando de lado a lado.',
            ],
            [
                'name' => 'Elevaciones de talones sentado',
                'description' => 'Las elevaciones de talones sentado son un ejercicio de aislamiento que se enfoca en los músculos de las pantorrillas. Se realiza sentado en un banco o silla con las rodillas flexionadas y levantando los talones mientras se mantiene el cuerpo estable.',
            ],
            [
                'name' => 'Peso muerto rumano',
                'description' => 'El peso muerto rumano es un ejercicio de levantamiento de peso que se enfoca principalmente en los músculos de la espalda baja y los isquiotibiales. Se realiza manteniendo las piernas ligeramente flexionadas y doblando la cintura para bajar la barra hacia los tobillos y luego volviendo a la posición inicial.',
            ],
            [
                'name' => 'Press de hombros con mancuernas',
                'description' => 'El press de hombros con mancuernas es un ejercicio de entrenamiento de fuerza que se enfoca en los músculos de los hombros y tríceps. Se realiza de pie, levantando las mancuernas desde los hombros hasta una posición extendida sobre la cabeza.',
            ],
            [
                'name' => 'Curl concentrado',
                'description' => 'El curl concentrado es un ejercicio de aislamiento que se enfoca en los músculos de los brazos. Se realiza sentado, apoyando el codo en la pierna y levantando una pesa o mancuerna hacia el hombro

 sin mover el resto del cuerpo.',
            ],
            [
                'name' => 'Elevaciones posteriores',
                'description' => 'Las elevaciones posteriores son un ejercicio de aislamiento que se enfoca en los músculos de los hombros y la espalda. Se realiza de pie, levantando pesas desde el frente del cuerpo hasta que los brazos estén paralelos al suelo y luego llevándolas hacia atrás.',
            ],
            [
                'name' => 'Peso muerto sumo',
                'description' => 'El peso muerto sumo es una variante del peso muerto que se enfoca en los músculos de las piernas y glúteos. Se realiza con los pies más separados que el ancho de los hombros y se baja la barra manteniendo las rodillas flexionadas y la espalda recta.',
            ],
            [
                'name' => 'Elevaciones de rodillas',
                'description' => 'Las elevaciones de rodillas son un ejercicio de entrenamiento de fuerza que se enfoca en los músculos abdominales. Se realiza colgándose de una barra y levantando las rodillas hacia el pecho.',
            ],
            [
                'name' => 'Press de banca inclinado',
                'description' => 'El press de banca inclinado es un ejercicio de entrenamiento de fuerza que se enfoca en los músculos del pecho, hombros y tríceps. Se realiza acostado en un banco inclinado y empujando una barra hacia arriba y hacia abajo.',
            ],
            [
                'name' => 'Dominadas con agarre estrecho',
                'description' => 'Las dominadas con agarre estrecho son un ejercicio de entrenamiento de fuerza que se enfoca en los músculos de la espalda y los brazos. Se realiza colgándose de una barra con las manos más cerca una de la otra y levantando el cuerpo hasta que la barbilla esté por encima de la barra.',
            ],
            [
                'name' => 'Fondos de tríceps en paralelas',
                'description' => 'Los fondos de tríceps en paralelas son un ejercicio de entrenamiento de fuerza que se enfoca en los músculos del tríceps. Se realiza apoyando las manos en barras paralelas y bajando el cuerpo flexionando los codos.',
            ],
            [
                'name' => 'Remo con mancuernas',
                'description' => 'El remo con mancuernas es un ejercicio que trabaja los músculos de la espalda, los hombros y los brazos. Se realiza inclinándose hacia adelante con las rodillas ligeramente flexionadas y levantando las mancuernas hacia el pecho.',
            ],
            [
                'name' => 'Press de hombros con barra',
                'description' => 'El press de hombros con barra es un ejercicio de entrenamiento de fuerza que se enfoca en los músculos de los hombros y tríceps. Se realiza de pie, levantando una barra desde los hombros hasta una posición extendida sobre la cabeza.',
            ],
            [
                'name' => 'Curl con barra',
                'description' => 'El curl con barra es un ejercicio de aislamiento que se enfoca en

 los músculos de los brazos. Se realiza levantando una barra desde la posición inicial con los brazos extendidos hasta la contracción del bíceps.',
            ],
            [
                'name' => 'Elevaciones frontales alternas',
                'description' => 'Las elevaciones frontales alternas son un ejercicio de aislamiento que se enfoca en los músculos de los hombros. Se realiza de pie, levantando pesas desde el frente del cuerpo alternando los brazos hasta que los brazos estén paralelos al suelo.',
            ],
            [
                'name' => 'Sentadillas con salto',
                'description' => 'Las sentadillas con salto son un ejercicio compuesto que trabaja los músculos de las piernas y glúteos. Se realiza flexionando las rodillas y caderas mientras se mantiene la espalda recta y luego saltando explosivamente hacia arriba.',
            ],
            [
                'name' => 'Peso muerto rumano con mancuernas',
                'description' => 'El peso muerto rumano con mancuernas es un ejercicio de levantamiento de peso que se enfoca principalmente en los músculos de la espalda baja y los isquiotibiales. Se realiza manteniendo las piernas ligeramente flexionadas y doblando la cintura para bajar las mancuernas hacia los tobillos y luego volviendo a la posición inicial.',
            ],
            [
                'name' => 'Press de hombros sentado',
                'description' => 'El press de hombros sentado es un ejercicio de entrenamiento de fuerza que se enfoca en los músculos de los hombros y tríceps. Se realiza sentado, levantando una barra o mancuernas desde los hombros hasta una posición extendida sobre la cabeza.',
            ],
            [
                'name' => 'Curl de concentración con mancuerna',
                'description' => 'El curl de concentración con mancuerna es un ejercicio de aislamiento que se enfoca en los músculos de los brazos. Se realiza sentado, apoyando el codo en la pierna y levantando una mancuerna hacia el hombro sin mover el resto del cuerpo.',
            ],
            [
                'name' => 'Elevaciones posteriores con mancuernas',
                'description' => 'Las elevaciones posteriores con mancuernas son un ejercicio de aislamiento que se enfoca en los músculos de los hombros y la espalda. Se realiza de pie, levantando las mancuernas desde el frente del cuerpo hasta que los brazos estén paralelos al suelo y luego llevándolas hacia atrás.',
            ],
            [
                'name' => 'Sentadillas búlgaras',
                'description' => 'Las sentadillas búlgaras son un ejercicio compuesto que trabaja los músculos de las piernas y glúteos. Se realiza con una pierna extendida hacia atrás y flexionando la rodilla de la pierna delantera para bajar el cuerpo hacia el suelo.',
            ],
            [
                'name' => 'Plancha',
                'description' => 'La plancha es un ejercicio de entrenamiento de fuerza que se enfoca en los músculos abdominales y de la parte superior del cuerpo. Se realiza apoyando los antebrazos y los dedos

 de los pies en el suelo, manteniendo el cuerpo en línea recta y sosteniendo la posición durante un período de tiempo determinado.',
            ],
            [
                'name' => 'Press de banca declinado',
                'description' => 'El press de banca declinado es un ejercicio de entrenamiento de fuerza que se enfoca en los músculos del pecho, hombros y tríceps. Se realiza acostado en un banco declinado y empujando una barra o mancuernas hacia arriba y hacia abajo.',
            ],
        ];

        return $exercises;
    }
}

$exerciseGenerator = new ExerciseGenerator();
$exercises = $exerciseGenerator->getExercises();

foreach ($exercises as $exercise) {
    echo $exercise['name'] . ': ' . $exercise['description'] . '\n';
}
