# Ontologia de alérgenos

## Descrição
 Essa ontologia tem o objetivo de categorizar ou classificar alimentos com base em substâncias alergênicas, de forma a representar formalmente os principais alérgenos reconhecidos pelo consenso brasileiro sobre alergia alimentar, seus ingredientes associados e os alimentos que os contêm. Pretendemos responder as seguintes perguntas com essa ontologia:
<ul>
  <li>Uma pessoa alérgica a um Alimento X pode comer o alimento Y ?</li>
  <li>Quais são os alérgenos mais comuns em produtos P ?</li>
  <li>Quais alimentos o paciente tem alergia alimentar ?</li>
  <li>Quais alimentos foram consumidos pelo paciente Z no período T ?</li>
  <li>Quais alergênicos estão presentes na composição do alimento Y ?</li>
  <li>Quais alternativas seguras existem ao alimento Y para o paciente Z ?</li>
  <li>Quais alimentos comumente causam reações alérgicas entre pacientes com perfil semelhante ao do paciente Z ?</li>
  <li>Quais alimentos não contém o alérgeno X ?</li>
  <li>Quais são os principais alérgenos alimentares no Brasil, de acordo com o consenso brasileiro sobre alergia alimentar ?</li>
</ul>


## Visões da ontologia

### Visão central

 ![Visão central](https://github.com/user-attachments/assets/ef8d4ac0-db8b-4988-8135-4d0a03ebeb0a)

 Essa visão representa o processo da alergia desde quando o paciente ingere o alérgeno até o tratamento, classificando conceitos fundamentais desse processo.

### Visão de alérgenos

![Alérgenos](https://github.com/user-attachments/assets/54eb790b-8707-4917-9623-129606f78fe3)

Essa visão representa alguns dos principais alimentos alergênicos e suas composições proteicas.

### Visão de reaçoes alérgicas

![Reações alérgicas](https://github.com/user-attachments/assets/da0ca83c-bca4-44ee-b715-0aec590baf78)

Essa visão representa e classifica algumas reações alérgicas.

### Visão de reatividade cruzada

![Reatividade cruzada](https://github.com/user-attachments/assets/58031681-0279-41d6-893d-edc15309edf5)

Essa visão representa as relações de reatividade cruzada entre alimentos.


## Classes da Ontologia


### Classes Primitivas

<ul>
  <li>Alimento</li>
  <li>Pessoa</li>
  Subclasses:
  <ul> 
    <li>Medico</li>
    <li>Paciente</li>
  </ul>
 <li>Diagnostico</li>
 Subclasses:
 <ul>
  <li>Autorreferida</li>
  <li>ConfirmadaPorTesteDeProvocaoOral</li>
  <li>IdentificadaPorTesteCutaneo</li>
  <li>PresencaDeIgESericaEspecifica</li>
  <li>PrevalenciaPontual</li>
 </ul>
 <li>Tratamento</li>
  Subclasses:
  <ul>
    <li>DietaDeExclusao</li>
    <li>Dilatacoes</li>
    <li>UsoDeMedicamentos</li>
  </ul>
  <li>Alergia</li>
  <li>Substancia</li>
  Subclasses:
  <ul>
    <li>Carboidrato</li>
    Subclasses:
    <ul>
      <li>AlfaGal</li>
      <li>FucosesOuXiloses</li>
    </ul>
    <li>ProteinaAlimentar</li>
    Subclasses:
    <ul>
      <li>Albuminas</li>
      Subclasses:
      <ul>
        <li>Aglutininas</li>
        <li>Fosfolipases</li>
        <li>GlicoproteinasLecitinoReativas</li>
        <li>InibidoresDeAAmilase</li>
        <li>InibidoresDeProtease</li>
      </ul>
      <li>Caseinas</li>
      Subclasses:
      <ul>
        <li>AlfasCaseinas</li>
        <li>BetasCaseinas</li>
        <li>GamaCaseinas</li>
        <li>KappaCaseinas</li>
      </ul>
      <li>Globulinas</li>
      Subclasses:
      <ul>
        <li>Araquina</li>
        <li>Conaraquina</li>
      </ul>
      <li>ProteinasDoSoro</li>
      Subclasses:
      <ul>
        <li>Albumina</li>
        <li>alfaLactoalbumina</li>
        <li>betaLactoglobulina</li>
        <li>Imunoglobulinas</li>
        <li>ProteasesEPeptonas</li>
        <li>ProteinasDoSangue</li>
      </ul>
    </ul>
  </ul>
<li>ReacaoAdversaAAlimento</li>
Subclasses:
<ul>
  <li>MediadasPorIgE</li>
  Subclasses:
  <ul>
    <li>Angioderma</li>
    <li>Urticaria</li>
  </ul>
  <li>Mistas</li>
   Subclasses:
  <ul>
    <li>Asma</li>
    <li>DermatiteAtopica</li>
    <li>EsofagiteEosinofifilcaEoE</li>
    <li>GastriteEosinofilica</li>
    <li>GastroenteriteEosinofilica</li>
  </ul>
  <li>NaoMediadasPorIgE</li>
   Subclasses:
  <ul>
    <li>DermatiteDeContato</li>
    <li>DermatiteHerpetiforme</li>
  </ul>
</ul>

</ul>

### Classes Definidas

<ul>
  <li>Amendoim</li>
  <li>LeiteDeVaca</li>
  <li>Adulto</li>
  <li>Crianca</li>
</ul>


## Propriedades de Objeto

  Diagnstica
  <ul>
    <li>Domain: Medico</li>
    <li>Range: Paciente</li>
  </ul>
  Trata
  <ul>
    <li>Domain: Medico</li>
    <li>Range: Paciente</li>
  </ul>
  TemAlergiaA
  <ul>
    <li>Domain: Paciente</li>
    <li>Range: Alimento</li>
  </ul>
  hasComponent
  <ul>
    <li>Domain: Alimento</li>
    <li>Range: Substancia</li>
  </ul>
  isComponentOf
  <ul>
    <li>Domain: Substancia </li>
    <li>Range: Alimento</li>
  </ul>
    mediates
  <ul>
    <li>Domain: Relator(alergia,Diagnostico,Tratamento...)</li>
    <li>Range: Endurant(Paciente,Medico,Alimento)</li>
  </ul>
   ParticipatedIn
  <ul>
    <li>Domain: Object(Paciente, Alimento)</li>
    <li>Range: Event(ReacaoAdversaAAlimento)</li>
  </ul>


## Propriedades de Dados

  hasAge
  <ul>
    <li>Domain: Pessoa</li>
    <li>Range: xsd:integer</li>
  </ul>

## Axiomas das Classes

#### Pessoa
<ul>
  <li> hasAge some xsd:integer</li>
</ul>

#### Adulto

<ul>
  <li>Pessoa</li>
  <li>hasAge some xsd:integer[>= 18]</li>
</ul>


#### Crianca

<ul>
  <li>Pessoa</li>
  <li>hasAge some xsd:integer[< 18]</li>
</ul>


#### Medico

<ul>
  <li>Pessoa</li>
  <li>inverse (mediates) some Diagnostico</li>
  <li>inverse (mediates) some Tratamento</li>
  <li>Diagnstica some Paciente</li>
  <li>Trata some Paciente</li>
</ul>

#### Paciente

<ul>
  <li>Pessoa</li>
  <li>inverse (mediates) some Alergia</li>
  <li>inverse (mediates) some Diagnostico</li>
  <li>inverse (mediates) some Tratamento</li>
  <li>TemAlergiaA some Alimento</li>
  <li>participatedIn some ReacaoAdversaAAlimento</li>
</ul>


#### Alimento

<ul>
  <li>inverse (mediates) some Alergia</li>
  <li>hasComponent some Substancia</li>
  <li>participatedIn some ReacaoAdversaAAlimento</li>
</ul>

#### Amendoim

<ul>
  <li>Alimento</li>
  <li>hasComponent some Albuminas</li>
  <li>hasComponent some Globulinas</li>
</ul>


#### LeiteDeVaca

<ul>
  <li>Alimento</li>
  <li>hasComponent some Caseinas</li>
  <li>hasComponent some ProteinasDoSoro</li>
</ul>

#### Substancia

<ul>
  <li>isComponentOf some Alimento</li>
</ul>


#### Alergeno

<ul>
  <li>Substancia</li>
  <li>isComponentOf min 1 (participatedIn min 1 ReacaoAdversaAAlimento)</li>
</ul>

#### Alergeno

<ul>
  <li>Substancia</li>
  <li>isComponentOf min 1 (participatedIn min 1 ReacaoAdversaAAlimento)</li>
</ul>


#### Alergia

<ul>
  <li>Relator</li>
  <li>mediates min 1 Alimento</li>
  <li>mediates min 1 Paciente</li>
</ul>


#### Diagnostico

<ul>
  <li>Relator</li>
  <li>mediates min 1 Medico</li>
  <li>mediates min 1 Paciente</li>
</ul>

#### Tratamento

<ul>
  <li>Relator</li>
  <li>mediates min 1 Medico</li>
  <li>mediates min 1 Paciente</li>
</ul>


#### ReacaoAdversaAAlimento

<ul>
  <li> Event</li>
  <li> inverse (participatedIn) some Alimento</li>
  <li> inverse (participatedIn) some Paciente</li>
</ul>


## Consultas Sparql












 



