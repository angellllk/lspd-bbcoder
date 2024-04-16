<script setup>
</script>

<template>
    <div>
    <h1>Daily Observation Report (DOR)</h1>
    <form @submit.prevent="generateBBCode" style="margin-top: 2rem;">
      <div class="form-group fixed-width mb-2">
        <label for="name">Nume candidat:</label>
        <input type="text" id="name" class="form-control" v-model="name">
      </div>
      <div class="form-group fixed-width mb-2">
        <label for="badge">Insigna:</label>
        <input type="number" id="badge" class="form-control" v-model="badge">
      </div>
      <div class="form-group fixed-width mb-2">
        <label for="phase">Phase:</label>
        <input type="number" id="phase" class="form-control" v-model="phase">
      </div>
      <div class="form-group fixed-width mb-2">
        <label for="callsign">Callsign:</label>
        <input type="text" id="callsign" class="form-control" v-model="callsign">
      </div>
      
      <div class="wrapped">
        <div class="form-group fixed-width mb-2">
          <label for="1">1. Stress control – Communicații și comportament</label>
          <select id="1" class="form-control" v-model="eval_1">
            <option value="C">C</option>
            <option value="S">S</option>
            <option value="NO">NO</option>
            <option value="NI">NI</option>
          </select>
        </div>
        <div class="form-group fixed-width mb-2">
          <label for="2">2. Luarea de decizii / rezolvarea porblemelor</label>
          <select id="2" class="form-control" v-model="eval_2">
            <option value="C">C</option>
            <option value="S">S</option>
            <option value="NO">NO</option>
            <option value="NI">NI</option>
          </select>
        </div>
        <div class="form-group fixed-width mb-2">
          <label for="3">3. Abilități de condus – stres moderat / situații</label>
          <select id="3" class="form-control" v-model="eval_3">
            <option value="C">C</option>
            <option value="S">S</option>
            <option value="NO">NO</option>
            <option value="NI">NI</option>
          </select>
        </div>
        <div class="form-group fixed-width mb-2">
          <label for="4">4. Field Performance – situații normale</label>
          <select id="4" class="form-control" v-model="eval_4">
            <option value="C">C</option>
            <option value="S">S</option>
            <option value="NO">NO</option>
            <option value="NI">NI</option>
          </select>
        </div>
        <div class="form-group fixed-width mb-2">
          <label for="5">5. Field Performance – situații sub presiunea stresului</label>
          <select id="5" class="form-control" v-model="eval_5">
            <option value="C">C</option>
            <option value="S">S</option>
            <option value="NO">NO</option>
            <option value="NI">NI</option>
          </select>
        </div>
        <div class="form-group fixed-width mb-2">
          <label for="6">6. Siguranța ofițerului – Contact/cover/pat down</label>
          <select id="6" class="form-control" v-model="eval_6">
            <option value="C">C</option>
            <option value="S">S</option>
            <option value="NO">NO</option>
            <option value="NI">NI</option>
          </select>
        </div>
        <div class="form-group fixed-width mb-2">
          <label for="7">7. Controlul prizonierului sau abilități investigative</label>
          <select id="7" class="form-control" v-model="eval_7">
            <option value="C">C</option>
            <option value="S">S</option>
            <option value="NO">NO</option>
            <option value="NI">NI</option>
          </select>
        </div>
        <div class="form-group fixed-width mb-2">
          <label for="8">8. Locații – Timp Răspuns/orientare/cunoașterea locațiilor</label>
          <select id="8" class="form-control" v-model="eval_8">
            <option value="C">C</option>
            <option value="S">S</option>
            <option value="NO">NO</option>
            <option value="NI">NI</option>
          </select>
        </div>
        <div class="form-group fixed-width mb-2">
          <label for="9">9. Luarea inițiativei</label>
          <select id="9" class="form-control" v-model="eval_9">
            <option value="C">C</option>
            <option value="S">S</option>
            <option value="NO">NO</option>
            <option value="NI">NI</option>
          </select>
        </div>
        <div class="form-group fixed-width mb-2">
          <label for="10">10. Opriri vehiculare/de persoane</label>
          <select id="10" class="form-control" v-model="eval_10">
            <option value="C">C</option>
            <option value="S">S</option>
            <option value="NO">NO</option>
            <option value="NI">NI</option>
          </select>
        </div>
        <div class="form-group fixed-width mb-2">
          <label for="11">11. Abilități de condus – normale / controlul vitezei</label>
          <select id="11" class="form-control" v-model="eval_11">
            <option value="C">C</option>
            <option value="S">S</option>
            <option value="NO">NO</option>
            <option value="NI">NI</option>
          </select>
        </div>
        <div class="form-group fixed-width mb-2">
          <label for="12">12. Folosirea stației radio</label>
          <select id="12" class="form-control" v-model="eval_12">
            <option value="C">C</option>
            <option value="S">S</option>
            <option value="NO">NO</option>
            <option value="NI">NI</option>
          </select>
        </div>
        <div class="form-group fixed-width mb-2">
          <label for="13">13. Redactare rapoarte</label>
          <select id="13" class="form-control" v-model="eval_13">
            <option value="C">C</option>
            <option value="S">S</option>
            <option value="NO">NO</option>
            <option value="NI">NI</option>
          </select>
        </div>
        <div class="form-group fixed-width mb-2">
          <label for="14">14. Arest – Cod penal/proceduri/legi/explicații</label>
          <select id="14" class="form-control" v-model="eval_14">
            <option value="C">C</option>
            <option value="S">S</option>
            <option value="NO">NO</option>
            <option value="NI">NI</option>
          </select>
        </div>
        <div class="form-group fixed-width mb-2">
          <label for="15">15. Politici și proceduri departamentaleAt</label>
          <select id="15" class="form-control" v-model="eval_15">
            <option value="C">C</option>
            <option value="S">S</option>
            <option value="NO">NO</option>
            <option value="NI">NI</option>
          </select>
        </div>
        <div class="form-group fixed-width mb-2">
          <label for="16">16. Codul penal</label>
          <select id="16" class="form-control" v-model="eval_16">
            <option value="C">C</option>
            <option value="S">S</option>
            <option value="NO">NO</option>
            <option value="NI">NI</option>
          </select>
        </div>
        <div class="form-group fixed-width mb-2">
          <label for="17">17. Infractiuni in trafic</label>
          <select id="17" class="form-control" v-model="eval_17">
            <option value="C">C</option>
            <option value="S">S</option>
            <option value="NO">NO</option>
            <option value="NI">NI</option>
          </select>
        </div>
        <div class="form-group fixed-width mb-2">
          <label for="18">18. Proceduri de patrula</label>
          <select id="18" class="form-control" v-model="eval_18">
            <option value="C">C</option>
            <option value="S">S</option>
            <option value="NO">NO</option>
            <option value="NI">NI</option>
          </select>
        </div>
        <div class="form-group fixed-width mb-2">
          <label for="19">19. Acceptarea feedback-ului/criticii</label>
          <select id="19" class="form-control" v-model="eval_19">
            <option value="C">C</option>
            <option value="S">S</option>
            <option value="NO">NO</option>
            <option value="NI">NI</option>
          </select>
        </div>
        <div class="form-group fixed-width mb-2">
          <label for="20">20. Atitudinea cu privire la munca de ofiter</label>
          <select id="20" class="form-control" v-model="eval_20">
            <option value="C">C</option>
            <option value="S">S</option>
            <option value="NO">NO</option>
            <option value="NI">NI</option>
          </select>
        </div>
        <div class="form-group fixed-width mb-2">
          <label for="21">21. Relația cu cetățenii</label>
          <select id="21" class="form-control" v-model="eval_21">
            <option value="C">C</option>
            <option value="S">S</option>
            <option value="NO">NO</option>
            <option value="NI">NI</option>
          </select>
        </div>
        <div class="form-group fixed-width mb-2">
          <label for="22">22. Relația cu alți angajați ai departamentului</label>
          <select id="22" class="form-control" v-model="eval_22">
            <option value="C">C</option>
            <option value="S">S</option>
            <option value="NO">NO</option>
            <option value="NI">NI</option>
          </select>
        </div>
        <div class="form-group fixed-width mb-2">
          <label for="23">23. Aspect general</label>
          <select id="23" class="form-control" v-model="eval_23">
            <option value="C">C</option>
            <option value="S">S</option>
            <option value="NO">NO</option>
            <option value="NI">NI</option>
          </select>
        </div>
        <div class="form-group fixed-width mb-2">
          <label for="24">24. Întrebări despre procedurile departamentului</label>
          <select id="24" class="form-control" v-model="eval_24">
            <option value="C">C</option>
            <option value="S">S</option>
            <option value="NO">NO</option>
            <option value="NI">NI</option>
          </select>
        </div>
        <div class="form-group fixed-width mb-2">
          <label for="25">25. Întrebări cu privire la Codul Penal</label>
          <select id="25" class="form-control" v-model="eval_25">
            <option value="C">C</option>
            <option value="S">S</option>
            <option value="NO">NO</option>
            <option value="NI">NI</option>
          </select>
        </div>
        <div class="form-group fixed-width mb-2">
          <label for="26">26. Calitatea Generală a Roleplay-ului</label>
          <select id="26" class="form-control" v-model="eval_26">
            <option value="C">C</option>
            <option value="S">S</option>
            <option value="NO">NO</option>
            <option value="NI">NI</option>
          </select>
        </div>
        <div class="form-group fixed-width mb-2">
          <label for="27">27. Portretizarea Caracterului</label>
          <select id="27" class="form-control" v-model="eval_27">
            <option value="C">C</option>
            <option value="S">S</option>
            <option value="NO">NO</option>
            <option value="NI">NI</option>
          </select>
        </div>
        <div class="form-group fixed-width mb-2">
          <label for="28">28. Atitudine OOC</label>
          <select id="28" class="form-control" v-model="eval_28">
            <option value="C">C</option>
            <option value="S">S</option>
            <option value="NO">NO</option>
            <option value="NI">NI</option>
          </select>
        </div>
      </div>

      <div class="form-group fixed-width mb-2">
        <label for="narrative">Narativ:</label>
        <textarea type="text" id="narrative" class="form-control" v-model="narrative" placeholder="00:00 - am inceput tura 
12:00 - situatie, descriere, ofiterul a facut X...
15:00 - am terminat tura">
        </textarea>
      </div>
      <div class="form-group fixed-width mb-2">
        <label for="name_fto">Nume FTO:</label>
        <input type="text" id="name_fto" class="form-control" v-model="name_fto">
      </div>
      <div class="form-group fixed-width mb-2">
        <label for="signature">Semnatura:</label>
        <input type="text" id="signature" class="form-control" v-model="signature">
      </div>
      <button type="submit" class="btn btn-secondary mt-3">Genereaza BBCode</button>
    </form>

    <div v-if="bbCode" class="mt-5">
        <section id="res">
        <h2>DOR BBCode:</h2> <button @click="selectAll">Select All</button>
        <br>
        <textarea id="select" ref="bbCodeTextArea" rows="10" readonly>{{ bbCode }}</textarea> 
      </section>
    </div>
    
  </div>

</template>

<script>
export default {
  data() {
    return {
      name: '',
      badge: '',
      phase: '',
      callsign: '',
      eval_1: '',
      eval_2: '',
      eval_3: '',
      eval_4: '',
      eval_5: '',
      eval_6: '',
      eval_7: '',
      eval_8: '',
      eval_9: '',
      eval_10: '',
      eval_11: '',
      eval_12: '',
      eval_13: '',
      eval_14: '',
      eval_15: '',
      eval_16: '',
      eval_17: '',
      eval_18: '',
      eval_19: '',
      eval_20: '',
      eval_21: '',
      eval_22: '',
      eval_23: '',
      eval_24: '',
      eval_25: '',
      eval_26: '',
      eval_27: '',
      eval_28: '',
      narrative: '',
      name_fto: '',
      signature: '',
      bbCode: ''
    };
  },
  methods: {
    selectAll() {
      const textarea = this.$el.querySelector('#select');
      textarea.select();
    },

    generateBBCode() {
      this.bbCode = `[divbox=white][hr][/hr][center][color=black][size=85][b]LOS SANTOS POLICE DEPARTMENT
      DAILY OBSERVATION REPORT[/b][/size][/color][/center][hr][/hr][table]
      [tr]
      [td]
      [color=black][size=80][b]NUME CANDIDAT[/b]
      [/size][/color][/td][td]
      [color=black][size=80][b]INSIGNĂ[/b]
      [/size][/color][/td][td]
      [color=black][size=80][b]PHASE[/b]
      [/size][/color][/td][td]
      [color=black][size=80][b]CALLSIGN[/b][/size][/color]
      [/td][/tr]
      [tr][td][size=80]     ${this.name}
      [/size][/td]
      [td][size=80]    ${this.badge}
      [/size][/td]
      [td][size=80]     ${this.phase}
      [/size][/td]
      [td][size=80]     ${this.callsign}
      [/size][/td][/tr]
      [/table][hr][/hr][table]
      [tr][td][center][color=black][size=80][b]EVALUARE CATEGORIALĂ[/b][/size][/color][/center][/td][/tr]
      [/table][hr][/hr]
      [table][tr][td]
      [color=black][size=80][b]Critical Performance Tasks[/b][/size][/color]
      [/td]
      [td][color=black][size=80][b][center]CALIFICATIV[/center][/b][/size][/color][/td][/tr]
      [tr][td]
      [color=black][size=80]1. Stress control – Communicații și comportament[/size][/color][/td]
      [td][center][color=black][size=80]      ${this.eval_1}
      [/size][/color][/center]
      [/td][/tr][tr][td]
      [color=black][size=80]2. Luarea de decizii / rezolvarea porblemelor[/size][/color][/td]
      [td][center][color=black][size=80]      ${this.eval_2}
      [/size][/color][/center]
      [/td]
      [/tr][tr]
      [td]
      [color=black][size=80]3. Abilități de condus – stres moderat / situații[/size][/color][/td]
      [td][center][color=black][size=80]     ${this.eval_3}
      [/size][/color][/center]
      [/td]
      [/tr]
      [tr]
      [td]
      [color=black][size=80]4. Field Performance – situații normale[/size][/color][/td]
      [td][center][color=black][size=80]      ${this.eval_4}
      [/size][/color][/center]
      [/td]
      [/tr][tr]
      [td]
      [color=black][size=80]5. Field Performance – situații sub presiunea stresului[/size][/color][/td]
      [td][center][color=black][size=80]      ${this.eval_5}
      [/size][/color][/center]
      [/td]
      [/tr][tr]
      [td]
      [color=black][size=80]6. Siguranța ofițerului – Contact/cover/pat down[/size][/color][/td]
      [td]
      [center][color=black][size=80]      ${this.eval_6}
      [/size][/color][/center]
      [/td]
      [/tr][tr]
      [td]
      [color=black][size=80]7. Controlul prizonierului sau abilități investigative[/size][/color][/td]
      [td][center][color=black][size=80]      ${this.eval_7}
      [/size][/color][/center]
      [/td]
      [/tr][tr]
      [td]
      [color=black][size=80]8. Locații – Timp Răspuns/orientare/cunoașterea locațiilor[/size][/color][/td]
      [td][center][color=black][size=80]      ${this.eval_8}
      [/size][/color][/center]
      [/td]
      [/tr]
      [tr]
      [td]
      [color=black][size=80]9. Luarea inițiativei[/size][/color][/td]
      [td][center][color=black][size=80]      ${this.eval_9}
      [/size][/color][/center]
      [/td]
      [/tr]
      [tr]
      [td]
      [color=black][size=80]10. Opriri vehiculare/de persoane[/size][/color][/td]
      [td][center][color=black][size=80]      ${this.eval_10}
      [/size][/color][/center]
      [/td]
      [/tr][/table]

      [hr][/hr]

      [table][tr][td]
      [color=black][size=80][b]Performante frecvente[/b][/size][/color]
      [/td]
      [td][color=black][size=80][b][center]CALIFICATIV[/center][/b][/size][/color][/td][/tr]
      [tr][td]
      [color=black][size=80]11. Abilități de condus – normale / controlul vitezei[color=#FFFFFF]AAAAA[/color][/size][/color][/td]
      [td][center][color=black][size=80]      ${this.eval_11}
      [/size][/color][/center]
      [/td][/tr][tr][td]
      [color=black][size=80]12. Folosirea stației radio[/size][/color][/td]
      [td][center][color=black][size=80]      ${this.eval_12}
      [/size][/color][/center]
      [/td]
      [/tr][tr]
      [td]
      [color=black][size=80]13. Redactare rapoarte[/size][/color][/td]
      [td][center][color=black][size=80]      ${this.eval_13}
      [/size][/color][/center]
      [/td]
      [/tr]
      [tr]
      [td]
      [color=black][size=80]14. Arest – Cod penal/proceduri/legi/explicații[/size][/color][/td]
      [td][center][color=black][size=80]      ${this.eval_14}
      [/size][/color][/center]
      [/td][/tr][/table]
      [hr][/hr]
      [table][tr][td]
      [color=black][size=80][b]Cunoștințe[/b][/size][/color]
      [/td]
      [td][color=black][size=80][b][center]CALIFICATIV[/center][/b][/size][/color][/td][/tr]
      [tr][td]
      [color=black][size=80]15. Politici și proceduri departamentale[color=#FFFFFF]AAAAAAAAAAAAAAA[/color][/size][/color][/td]
      [td][center][color=black][size=80]      ${this.eval_15}
      [/size][/color][/center]
      [/td][/tr][tr][td]
      [color=black][size=80]16. Codul penal[/size][/color][/td]
      [td][center][color=black][size=80]      ${this.eval_16}
      [/size][/color][/center]
      [/td]
      [/tr][tr]
      [td]
      [color=black][size=80]17. Infractiuni in trafic[/size][/color][/td]
      [td][center][color=black][size=80]      ${this.eval_17}
      [/size][/color][/center]
      [/td]
      [/tr]
      [tr]
      [td][color=black][size=80]18. Proceduri de patrula[/size][/color][/td]
      [td][center][color=black][size=80]      ${this.eval_18}
      [/size][/color][/center]
      [/td][/tr][/table]
      [hr][/hr]

      [table][tr][td]
      [color=black][size=80][b]Atitudine și relații[/b][/size][/color]
      [/td]
      [td][color=black][size=80][b][center]CALIFICATIV[/center][/b][/size][/color][/td][/tr]
      [tr][td]
      [color=black][size=80]19. Acceptarea feedback-ului/criticii[color=#FFFFFF]AAAAAAAAAAAAAAAAA[/color][/size][/color][/td]
      [td][center][color=black][size=80]      ${this.eval_19}
      [/size][/color][/center]
      [/td][/tr][tr][td]
      [color=black][size=80]20. Atitudinea cu privire la munca de ofiter[/size][/color][/td]
      [td][center][color=black][size=80]      ${this.eval_20}
      [/size][/color][/center]
      [/td]
      [/tr][tr]
      [td]
      [color=black][size=80]21. Relația cu cetățenii[/size][/color][/td]
      [td][center][color=black][size=80]      ${this.eval_21}
      [/size][/color][/center]
      [/td]
      [/tr]
      [tr]
      [td][color=black][size=80]22. Relația cu alți angajați ai departamentului[/size][/color][/td]
      [td][center][color=black][size=80]      ${this.eval_22}
      [/size][/color][/center]
      [/td][/tr][/table]
      [hr][/hr]

      [table][tr][td]
      [color=black][size=80][b]Aspect[/b][/size][/color]
      [/td]
      [td][color=black][size=80][b][center]CALIFICATIV[/center][/b][/size][/color][/td][/tr]
      [tr][td]
      [color=black][size=80]23. Aspect general[color=#FFFFFF]AAAAAAAAAASAFASGASGGSAaaAAAAAA[/color][/size][/color][/td]
      [td][center][color=black][size=80]      ${this.eval_23}
      [/size][/color][/center]
      [/td][/tr][/table]
      [hr][/hr]

      [table][tr][td]
      [color=black][size=80][b]TESTARE[/b][/size][/color]
      [/td]
      [td][color=black][size=80][b][center]CALIFICATIV[/center][/b][/size][/color][/td][/tr]
      [tr][td]
      [color=black][size=80]24. Întrebări despre procedurile departamentului[color=#FFFFFF]AAAAAAA[/color][/size][/color][/td]
      [td][center][color=black][size=80]      ${this.eval_24}
      [/size][/color][/center][/td][/tr]
      [tr][td][color=black][size=80]25. Întrebări cu privire la Codul Penal[/size][/color][/td]
      [td][center][color=black][size=80]      ${this.eval_25}
      [/size][/color][/center]
      [/td][/tr][/table]

      [hr][/hr]

      [table][tr][td]
      [color=black][size=80][b](( ROLEPLAY ))[/b][/size][/color]
      [/td]
      [td][color=black][size=80][b][center]CALIFICATIV[/center][/b][/size][/color][/td][/tr]
      [tr][td]
      [color=black][size=80]26. Calitatea Generală a Roleplay-ului[color=#FFFFFF]AAAAAAAAAAAAAAA[/color][/size][/color][/td]
      [td][center][color=black][size=80]      ${this.eval_26}
      [/size][/color][/center]
      [/td][/tr][tr][td]
      [color=black][size=80]27. Portretizarea Caracterului[/size][/color][/td]
      [td][center][color=black][size=80]      ${this.eval_27}
      [/size][/color][/center][/td][/tr]
      [tr][td]
      [color=black][size=80]28. Atitudine OOC[/size][/color][/td]
      [td][center][color=black][size=80]      ${this.eval_28}
      [/size][/color][/center][/td][/tr]
      [/table]
      [hr][/hr]

      [table]
      [tr]
      [td][center][size=80][b]EVALUAREA NARATIVĂ[/b][/size][/center][/td]
      [/tr]
      [/table][hr][/hr]
      [table]
      [tr]
      [td][size=80][b]NARATIV[/b][/size][/td][/tr]
      [tr][td][size=80]${this.narrative}
      [/size][/td]
      [/tr]
      [/table][hr][/hr][table]
      [tr][td][color=black][size=80][b]NUME FTO[/b][/td]
      [td][color=black][size=80][b]SEMNĂTURĂ[/b][/td][/tr]

      [tr][td][size=80]${this.name_fto}[/size][/td]
      [td][size=80]${this.signature}[/size][/td][/tr][/table]


      [/divbox]`;

       this.$nextTick(() => {
        this.$refs.bbCodeTextArea.focus();
      });
    }
  }
};
</script>

<style>
form {
  width: 30vw;
  font-size: 20px;
}

.wrapped {
  gap: 20px;
}

.form-column {
  flex: 1; /* Each column takes up equal space */
}

button {
  margin-top: 10px;
}

h1 {
  color: rgb(226, 226, 226);
}

.content {
  margin-top: 1rem;
  white-space: normal;
}

p {
  font-size: 24px;
}

textarea {
  width: 30vw;
}
</style>
