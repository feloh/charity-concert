<template>
<v-app>
<!--    <v-app-bar
        app
        color="#2b4d47"
        dark
    >
      <v-img
          max-width="40%"
          class="mx-auto mt-15"
          :src="require('@/assets/logo.png')"
      ></v-img>
    </v-app-bar>-->
<v-main
    class="application"
>
  <v-img
      :width="$vuetify.breakpoint.mdAndUp ? '50%' : '90%'"
      class="mx-auto mb-15"
      :src="description.src"
  ></v-img>
  <about
      :description="description"
      :donation="donation"
  />
  <auction
      :spirits="spirits"
      :mighties="mighties"
  />
  <v-img
      :width="$vuetify.breakpoint.mdAndUp ? '50%' : '70%'"
      class="mx-auto mb-15"
      :src="require('@/assets/participants.png')"
  ></v-img>
  <participant
      :participants="participants"
  >
  </participant>
</v-main>
<v-footer color="#ffff00">
  <v-expansion-panels
      class="application"
      accordion
      flat
  >
    <v-expansion-panel>
      <v-expansion-panel-header
          class="source-sans-pro"
      >
        Impressum
      </v-expansion-panel-header>
      <v-expansion-panel-content>
        <h1>Impressum</h1>
        <h2>Angaben gem&auml;&szlig; &sect; 5 TMG</h2>
        <p>
          Felix Lohmann<br/>
          Freiheit 2<br/>
          40789 Monheim
        </p>
        <h2>Kontakt</h2>
        <p>E-Mail: feloh@gmx.de</p>
      </v-expansion-panel-content>
    </v-expansion-panel>
    <v-expansion-panel>
      <v-expansion-panel-header
          class="source-sans-pro"
      >
        Datenschutz
      </v-expansion-panel-header>
      <v-expansion-panel-content>
        <h2>1. Datenschutz auf einen Blick</h2>
        <h3>Allgemeine Hinweise</h3> <p>Die folgenden Hinweise geben einen einfachen &Uuml;berblick dar&uuml;ber, was mit Ihren personenbezogenen Daten passiert, wenn Sie diese Website besuchen. Personenbezogene Daten sind alle Daten, mit denen Sie pers&ouml;nlich identifiziert werden k&ouml;nnen. Ausf&uuml;hrliche Informationen zum Thema Datenschutz entnehmen Sie unserer unter diesem Text aufgef&uuml;hrten Datenschutzerkl&auml;rung.</p>
        <h3>Datenerfassung auf dieser Website</h3> <h4>Wer ist verantwortlich f&uuml;r die Datenerfassung auf dieser Website?</h4> <p>Die Datenverarbeitung auf dieser Website erfolgt durch den Websitebetreiber. Dessen Kontaktdaten k&ouml;nnen Sie dem Abschnitt &bdquo;Hinweis zur Verantwortlichen Stelle&ldquo; in dieser Datenschutzerkl&auml;rung entnehmen.</p> <h4>Wie erfassen wir Ihre Daten?</h4> <p>Ihre Daten werden zum einen dadurch erhoben, dass Sie uns diese mitteilen. Hierbei kann es sich z.&nbsp;B. um Daten handeln, die Sie in ein Kontaktformular eingeben.</p> <p>Andere Daten werden automatisch oder nach Ihrer Einwilligung beim Besuch der Website durch unsere IT-Systeme erfasst. Das sind vor allem technische Daten (z.&nbsp;B. Internetbrowser, Betriebssystem oder Uhrzeit des Seitenaufrufs). Die Erfassung dieser Daten erfolgt automatisch, sobald Sie diese Website betreten.</p> <h4>Wof&uuml;r nutzen wir Ihre Daten?</h4> <p>Ein Teil der Daten wird erhoben, um eine fehlerfreie Bereitstellung der Website zu gew&auml;hrleisten. Andere Daten k&ouml;nnen zur Analyse Ihres Nutzerverhaltens verwendet werden.</p> <h4>Welche Rechte haben Sie bez&uuml;glich Ihrer Daten?</h4> <p>Sie haben jederzeit das Recht, unentgeltlich Auskunft &uuml;ber Herkunft, Empf&auml;nger und Zweck Ihrer gespeicherten personenbezogenen Daten zu erhalten. Sie haben au&szlig;erdem ein Recht, die Berichtigung oder L&ouml;schung dieser Daten zu verlangen. Wenn Sie eine Einwilligung zur Datenverarbeitung erteilt haben, k&ouml;nnen Sie diese Einwilligung jederzeit f&uuml;r die Zukunft widerrufen. Au&szlig;erdem haben Sie das Recht, unter bestimmten Umst&auml;nden die Einschr&auml;nkung der Verarbeitung Ihrer personenbezogenen Daten zu verlangen. Des Weiteren steht Ihnen ein Beschwerderecht bei der zust&auml;ndigen Aufsichtsbeh&ouml;rde zu.</p> <p>Hierzu sowie zu weiteren Fragen zum Thema Datenschutz k&ouml;nnen Sie sich jederzeit an uns wenden.</p>
        <h2>2. Hosting</h2>
        <h3>Externes Hosting</h3> <p>Diese Website wird bei einem externen Dienstleister gehostet (Hoster). Die personenbezogenen Daten, die auf dieser Website erfasst werden, werden auf den Servern des Hosters gespeichert. Hierbei kann es sich v. a. um IP-Adressen, Kontaktanfragen, Meta- und Kommunikationsdaten, Vertragsdaten, Kontaktdaten, Namen, Websitezugriffe und sonstige Daten, die &uuml;ber eine Website generiert werden, handeln.</p> <p>Der Einsatz des Hosters erfolgt zum Zwecke der Vertragserf&uuml;llung gegen&uuml;ber unseren potenziellen und bestehenden Kunden (Art. 6 Abs. 1 lit. b DSGVO) und im Interesse einer sicheren, schnellen und effizienten Bereitstellung unseres Online-Angebots durch einen professionellen Anbieter (Art. 6 Abs. 1 lit. f DSGVO).</p> <p>Unser Hoster wird Ihre Daten nur insoweit verarbeiten, wie dies zur Erf&uuml;llung seiner Leistungspflichten erforderlich ist und unsere Weisungen in Bezug auf diese Daten befolgen.</p> <p>Wir setzen folgenden Hoster ein:</p>
        <p>GitHub HQ, 88 Colin P Kelly Jr. Street, San Francisco, CA</p>
        <h2>3. Allgemeine Hinweise und Pflicht&shy;informationen</h2>
        <h3>Datenschutz</h3> <p>Die Betreiber dieser Seiten nehmen den Schutz Ihrer pers&ouml;nlichen Daten sehr ernst. Wir behandeln Ihre personenbezogenen Daten vertraulich und entsprechend den gesetzlichen Datenschutzvorschriften sowie dieser Datenschutzerkl&auml;rung.</p> <p>Wenn Sie diese Website benutzen, werden verschiedene personenbezogene Daten erhoben. Personenbezogene Daten sind Daten, mit denen Sie pers&ouml;nlich identifiziert werden k&ouml;nnen. Die vorliegende Datenschutzerkl&auml;rung erl&auml;utert, welche Daten wir erheben und wof&uuml;r wir sie nutzen. Sie erl&auml;utert auch, wie und zu welchem Zweck das geschieht.</p> <p>Wir weisen darauf hin, dass die Daten&uuml;bertragung im Internet (z.&nbsp;B. bei der Kommunikation per E-Mail) Sicherheitsl&uuml;cken aufweisen kann. Ein l&uuml;ckenloser Schutz der Daten vor dem Zugriff durch Dritte ist nicht m&ouml;glich.</p>
        <h3>Hinweis zur verantwortlichen Stelle</h3> <p>Die verantwortliche Stelle f&uuml;r die Datenverarbeitung auf dieser Website ist:</p> <p>Felix Lohmann <br />
        Freiheit 2<br />
        40789 Monheim</p>

        <p>Telefon: &#91;Telefonnummer der verantwortlichen Stelle&#93;<br />
          E-Mail: feloh@gmx.de</p>
        <p>Verantwortliche Stelle ist die nat&uuml;rliche oder juristische Person, die allein oder gemeinsam mit anderen &uuml;ber die Zwecke und Mittel der Verarbeitung von personenbezogenen Daten (z.&nbsp;B. Namen, E-Mail-Adressen o. &Auml;.) entscheidet.</p>

        <h3>Speicherdauer</h3> <p>Soweit innerhalb dieser Datenschutzerkl&auml;rung keine speziellere Speicherdauer genannt wurde, verbleiben Ihre personenbezogenen Daten bei uns, bis der Zweck f&uuml;r die Datenverarbeitung entf&auml;llt. Wenn Sie ein berechtigtes L&ouml;schersuchen geltend machen oder eine Einwilligung zur Datenverarbeitung widerrufen, werden Ihre Daten gel&ouml;scht, sofern wir keine anderen rechtlich zul&auml;ssigen Gr&uuml;nde f&uuml;r die Speicherung Ihrer personenbezogenen Daten haben (z.&nbsp;B. steuer- oder handelsrechtliche Aufbewahrungsfristen); im letztgenannten Fall erfolgt die L&ouml;schung nach Fortfall dieser Gr&uuml;nde.</p>
        <h3>Hinweis zur Datenweitergabe in die USA und sonstige Drittstaaten</h3> <p>Wir verwenden unter anderem Tools von Unternehmen mit Sitz in den USA oder sonstigen datenschutzrechtlich nicht sicheren Drittstaaten. Wenn diese Tools aktiv sind, k&ouml;nnen Ihre personenbezogene Daten in diese Drittstaaten &uuml;bertragen und dort verarbeitet werden. Wir weisen darauf hin, dass in diesen L&auml;ndern kein mit der EU vergleichbares Datenschutzniveau garantiert werden kann. Beispielsweise sind US-Unternehmen dazu verpflichtet, personenbezogene Daten an Sicherheitsbeh&ouml;rden herauszugeben, ohne dass Sie als Betroffener hiergegen gerichtlich vorgehen k&ouml;nnten. Es kann daher nicht ausgeschlossen werden, dass US-Beh&ouml;rden (z.&nbsp;B. Geheimdienste) Ihre auf US-Servern befindlichen Daten zu &Uuml;berwachungszwecken verarbeiten, auswerten und dauerhaft speichern. Wir haben auf diese Verarbeitungst&auml;tigkeiten keinen Einfluss.</p><h3>Widerruf Ihrer Einwilligung zur Datenverarbeitung</h3> <p>Viele Datenverarbeitungsvorg&auml;nge sind nur mit Ihrer ausdr&uuml;cklichen Einwilligung m&ouml;glich. Sie k&ouml;nnen eine bereits erteilte Einwilligung jederzeit widerrufen. Die Rechtm&auml;&szlig;igkeit der bis zum Widerruf erfolgten Datenverarbeitung bleibt vom Widerruf unber&uuml;hrt.</p>
        <h3>Widerspruchsrecht gegen die Datenerhebung in besonderen F&auml;llen sowie gegen Direktwerbung (Art. 21 DSGVO)</h3> <p>WENN DIE DATENVERARBEITUNG AUF GRUNDLAGE VON ART. 6 ABS. 1 LIT. E ODER F DSGVO ERFOLGT, HABEN SIE JEDERZEIT DAS RECHT, AUS GR&Uuml;NDEN, DIE SICH AUS IHRER BESONDEREN SITUATION ERGEBEN, GEGEN DIE VERARBEITUNG IHRER PERSONENBEZOGENEN DATEN WIDERSPRUCH EINZULEGEN; DIES GILT AUCH F&Uuml;R EIN AUF DIESE BESTIMMUNGEN GEST&Uuml;TZTES PROFILING. DIE JEWEILIGE RECHTSGRUNDLAGE, AUF DENEN EINE VERARBEITUNG BERUHT, ENTNEHMEN SIE DIESER DATENSCHUTZERKL&Auml;RUNG. WENN SIE WIDERSPRUCH EINLEGEN, WERDEN WIR IHRE BETROFFENEN PERSONENBEZOGENEN DATEN NICHT MEHR VERARBEITEN, ES SEI DENN, WIR K&Ouml;NNEN ZWINGENDE SCHUTZW&Uuml;RDIGE GR&Uuml;NDE F&Uuml;R DIE VERARBEITUNG NACHWEISEN, DIE IHRE INTERESSEN, RECHTE UND FREIHEITEN &Uuml;BERWIEGEN ODER DIE VERARBEITUNG DIENT DER GELTENDMACHUNG, AUS&Uuml;BUNG ODER VERTEIDIGUNG VON RECHTSANSPR&Uuml;CHEN (WIDERSPRUCH NACH ART. 21 ABS. 1 DSGVO).</p> <p>WERDEN IHRE PERSONENBEZOGENEN DATEN VERARBEITET, UM DIREKTWERBUNG ZU BETREIBEN, SO HABEN SIE DAS RECHT, JEDERZEIT WIDERSPRUCH GEGEN DIE VERARBEITUNG SIE BETREFFENDER PERSONENBEZOGENER DATEN ZUM ZWECKE DERARTIGER WERBUNG EINZULEGEN; DIES GILT AUCH F&Uuml;R DAS PROFILING, SOWEIT ES MIT SOLCHER DIREKTWERBUNG IN VERBINDUNG STEHT. WENN SIE WIDERSPRECHEN, WERDEN IHRE PERSONENBEZOGENEN DATEN ANSCHLIESSEND NICHT MEHR ZUM ZWECKE DER DIREKTWERBUNG VERWENDET (WIDERSPRUCH NACH ART. 21 ABS. 2 DSGVO).</p>
        <h3>Beschwerde&shy;recht bei der zust&auml;ndigen Aufsichts&shy;beh&ouml;rde</h3> <p>Im Falle von Verst&ouml;&szlig;en gegen die DSGVO steht den Betroffenen ein Beschwerderecht bei einer Aufsichtsbeh&ouml;rde, insbesondere in dem Mitgliedstaat ihres gew&ouml;hnlichen Aufenthalts, ihres Arbeitsplatzes oder des Orts des mutma&szlig;lichen Versto&szlig;es zu. Das Beschwerderecht besteht unbeschadet anderweitiger verwaltungsrechtlicher oder gerichtlicher Rechtsbehelfe.</p>
        <h3>Recht auf Daten&shy;&uuml;bertrag&shy;barkeit</h3> <p>Sie haben das Recht, Daten, die wir auf Grundlage Ihrer Einwilligung oder in Erf&uuml;llung eines Vertrags automatisiert verarbeiten, an sich oder an einen Dritten in einem g&auml;ngigen, maschinenlesbaren Format aush&auml;ndigen zu lassen. Sofern Sie die direkte &Uuml;bertragung der Daten an einen anderen Verantwortlichen verlangen, erfolgt dies nur, soweit es technisch machbar ist.</p>
        <h3>Auskunft, L&ouml;schung und Berichtigung</h3> <p>Sie haben im Rahmen der geltenden gesetzlichen Bestimmungen jederzeit das Recht auf unentgeltliche Auskunft &uuml;ber Ihre gespeicherten personenbezogenen Daten, deren Herkunft und Empf&auml;nger und den Zweck der Datenverarbeitung und ggf. ein Recht auf Berichtigung oder L&ouml;schung dieser Daten. Hierzu sowie zu weiteren Fragen zum Thema personenbezogene Daten k&ouml;nnen Sie sich jederzeit an uns wenden.</p>
        <h3>Recht auf Einschr&auml;nkung der Verarbeitung</h3> <p>Sie haben das Recht, die Einschr&auml;nkung der Verarbeitung Ihrer personenbezogenen Daten zu verlangen. Hierzu k&ouml;nnen Sie sich jederzeit an uns wenden. Das Recht auf Einschr&auml;nkung der Verarbeitung besteht in folgenden F&auml;llen:</p> <ul> <li>Wenn Sie die Richtigkeit Ihrer bei uns gespeicherten personenbezogenen Daten bestreiten, ben&ouml;tigen wir in der Regel Zeit, um dies zu &uuml;berpr&uuml;fen. F&uuml;r die Dauer der Pr&uuml;fung haben Sie das Recht, die Einschr&auml;nkung der Verarbeitung Ihrer personenbezogenen Daten zu verlangen.</li> <li>Wenn die Verarbeitung Ihrer personenbezogenen Daten unrechtm&auml;&szlig;ig geschah/geschieht, k&ouml;nnen Sie statt der L&ouml;schung die Einschr&auml;nkung der Datenverarbeitung verlangen.</li> <li>Wenn wir Ihre personenbezogenen Daten nicht mehr ben&ouml;tigen, Sie sie jedoch zur Aus&uuml;bung, Verteidigung oder Geltendmachung von Rechtsanspr&uuml;chen ben&ouml;tigen, haben Sie das Recht, statt der L&ouml;schung die Einschr&auml;nkung der Verarbeitung Ihrer personenbezogenen Daten zu verlangen.</li> <li>Wenn Sie einen Widerspruch nach Art. 21 Abs. 1 DSGVO eingelegt haben, muss eine Abw&auml;gung zwischen Ihren und unseren Interessen vorgenommen werden. Solange noch nicht feststeht, wessen Interessen &uuml;berwiegen, haben Sie das Recht, die Einschr&auml;nkung der Verarbeitung Ihrer personenbezogenen Daten zu verlangen.</li> </ul> <p>Wenn Sie die Verarbeitung Ihrer personenbezogenen Daten eingeschr&auml;nkt haben, d&uuml;rfen diese Daten &ndash; von ihrer Speicherung abgesehen &ndash; nur mit Ihrer Einwilligung oder zur Geltendmachung, Aus&uuml;bung oder Verteidigung von Rechtsanspr&uuml;chen oder zum Schutz der Rechte einer anderen nat&uuml;rlichen oder juristischen Person oder aus Gr&uuml;nden eines wichtigen &ouml;ffentlichen Interesses der Europ&auml;ischen Union oder eines Mitgliedstaats verarbeitet werden.</p>
        <h2>4. Datenerfassung auf dieser Website</h2>
        <h3>Anfrage per E-Mail, Telefon oder Telefax</h3> <p>Wenn Sie uns per E-Mail, Telefon oder Telefax kontaktieren, wird Ihre Anfrage inklusive aller daraus hervorgehenden personenbezogenen Daten (Name, Anfrage) zum Zwecke der Bearbeitung Ihres Anliegens bei uns gespeichert und verarbeitet. Diese Daten geben wir nicht ohne Ihre Einwilligung weiter.</p> <p>Die Verarbeitung dieser Daten erfolgt auf Grundlage von Art. 6 Abs. 1 lit. b DSGVO, sofern Ihre Anfrage mit der Erf&uuml;llung eines Vertrags zusammenh&auml;ngt oder zur Durchf&uuml;hrung vorvertraglicher Ma&szlig;nahmen erforderlich ist. In allen &uuml;brigen F&auml;llen beruht die Verarbeitung auf unserem berechtigten Interesse an der effektiven Bearbeitung der an uns gerichteten Anfragen (Art. 6 Abs. 1 lit. f DSGVO) oder auf Ihrer Einwilligung (Art. 6 Abs. 1 lit. a DSGVO) sofern diese abgefragt wurde.</p> <p>Die von Ihnen an uns per Kontaktanfragen &uuml;bersandten Daten verbleiben bei uns, bis Sie uns zur L&ouml;schung auffordern, Ihre Einwilligung zur Speicherung widerrufen oder der Zweck f&uuml;r die Datenspeicherung entf&auml;llt (z.&nbsp;B. nach abgeschlossener Bearbeitung Ihres Anliegens). Zwingende gesetzliche Bestimmungen &ndash; insbesondere gesetzliche Aufbewahrungsfristen &ndash; bleiben unber&uuml;hrt.</p>
        <h2>5. Plugins und Tools</h2>
        <h3>Google Web Fonts</h3> <p>Diese Seite nutzt zur einheitlichen Darstellung von Schriftarten so genannte Web Fonts, die von Google bereitgestellt werden. Beim Aufruf einer Seite l&auml;dt Ihr Browser die ben&ouml;tigten Web Fonts in ihren Browsercache, um Texte und Schriftarten korrekt anzuzeigen.</p> <p>Zu diesem Zweck muss der von Ihnen verwendete Browser Verbindung zu den Servern von Google aufnehmen. Hierdurch erlangt Google Kenntnis dar&uuml;ber, dass &uuml;ber Ihre IP-Adresse diese Website aufgerufen wurde. Die Nutzung von Google WebFonts erfolgt auf Grundlage von Art. 6 Abs. 1 lit. f DSGVO. Der Websitebetreiber hat ein berechtigtes Interesse an der einheitlichen Darstellung des Schriftbildes auf seiner Website. Sofern eine entsprechende Einwilligung abgefragt wurde (z.&nbsp;B. eine Einwilligung zur Speicherung von Cookies), erfolgt die Verarbeitung ausschlie&szlig;lich auf Grundlage von Art. 6 Abs. 1 lit. a DSGVO; die Einwilligung ist jederzeit widerrufbar.</p> <p>Wenn Ihr Browser Web Fonts nicht unterst&uuml;tzt, wird eine Standardschrift von Ihrem Computer genutzt.</p> <p>Weitere Informationen zu Google Web Fonts finden Sie unter <a href="https://developers.google.com/fonts/faq" target="_blank" rel="noopener noreferrer">https://developers.google.com/fonts/faq</a> und in der Datenschutzerkl&auml;rung von Google: <a href="https://policies.google.com/privacy?hl=de" target="_blank" rel="noopener noreferrer">https://policies.google.com/privacy?hl=de</a>.</p>
        <p>Quelle: <a href="https://www.e-recht24.de">https://www.e-recht24.de</a></p>
      </v-expansion-panel-content>
    </v-expansion-panel>
    <v-expansion-panel>
      <v-expansion-panel-header
          class="source-sans-pro"
      >
        Disclaimer
      </v-expansion-panel-header>
      <v-expansion-panel-content>
        <h1>Disclaimer</h1>
        <h2>Haftung für Inhalte</h2>
        <p>Als Diensteanbieter sind wir gemäß § 7 Abs.1 TMG für eigene Inhalte auf diesen Seiten nach den allgemeinen Gesetzen verantwortlich. Nach §§ 8 bis 10 TMG sind wir als Diensteanbieter jedoch nicht verpflichtet, übermittelte oder gespeicherte fremde Informationen zu überwachen oder nach Umständen zu forschen, die auf eine rechtswidrige Tätigkeit hinweisen.</p>
        <p>Verpflichtungen zur Entfernung oder Sperrung der Nutzung von Informationen nach den allgemeinen Gesetzen bleiben hiervon unberührt. Eine diesbezügliche Haftung ist jedoch erst ab dem Zeitpunkt der Kenntnis einer konkreten Rechtsverletzung möglich. Bei Bekanntwerden von entsprechenden Rechtsverletzungen werden wir diese Inhalte umgehend entfernen.</p>
        <h2>Haftung für Links</h2>
        <p>Unser Angebot enthält Links zu externen Websites Dritter, auf deren Inhalte wir keinen Einfluss haben. Deshalb können wir für diese fremden Inhalte auch keine Gewähr übernehmen. Für die Inhalte der verlinkten Seiten ist stets der jeweilige Anbieter oder Betreiber der Seiten verantwortlich. Die verlinkten Seiten wurden zum Zeitpunkt der Verlinkung auf mögliche Rechtsverstöße überprüft. Rechtswidrige Inhalte waren zum Zeitpunkt der Verlinkung nicht erkennbar.</p>
        <p>Eine permanente inhaltliche Kontrolle der verlinkten Seiten ist jedoch ohne konkrete Anhaltspunkte einer Rechtsverletzung nicht zumutbar. Bei Bekanntwerden von Rechtsverletzungen werden wir derartige Links umgehend entfernen.</p>
        <h2>Urheberrecht</h2>
        <p>Die durch die Seitenbetreiber erstellten Inhalte und Werke auf diesen Seiten unterliegen dem deutschen Urheberrecht. Die Vervielfältigung, Bearbeitung, Verbreitung und jede Art der Verwertung außerhalb der Grenzen des Urheberrechtes bedürfen der schriftlichen Zustimmung des jeweiligen Autors bzw. Erstellers. Downloads und Kopien dieser Seite sind nur für den privaten, nicht kommerziellen Gebrauch gestattet.</p>
        <p>Soweit die Inhalte auf dieser Seite nicht vom Betreiber erstellt wurden, werden die Urheberrechte Dritter beachtet. Insbesondere werden Inhalte Dritter als solche gekennzeichnet. Sollten Sie trotzdem auf eine Urheberrechtsverletzung aufmerksam werden, bitten wir um einen entsprechenden Hinweis. Bei Bekanntwerden von Rechtsverletzungen werden wir derartige Inhalte umgehend entfernen.</p>
      </v-expansion-panel-content>
    </v-expansion-panel>
  </v-expansion-panels>
</v-footer>
</v-app>
</template>

<script>
import About from '@/components/About'
import Auction from '@/components/Auction'
import Participant from "@/components/Participant";

export default {
  name: 'App',
  components: {
    Participant,
    About,
    Auction
  },
  data: () => ({
    description: {
      src: require('@/assets/aahr_logo.jpg'),
      title: require('@/assets/description_title.png'),
      help: require('@/assets/help.png'),
      lineUp: require('@/assets/lineUp.png'),
      text: 'Am 20.08.21 wird in der Monheimer Altstadt gemeinsam für den guten Zweck gefeiert. Alle Spenden gehen nach Dernau an die Ahr. Wie kann man helfen Wie kann man helfen? Komm einfach vorbei, genießt handgemachte Live-Musik auf der großen Altstadtbühne und habt ein pralles Portemonnaie für Spenden dabei. Alles Künstler treten umsonst auf. Wir gehen mit dem Hut der selbstverständlich in den großen Sammeltopf kommt. Kalte Getränke frisch vom Fass sowie leckere Snacks warten neben dem Bühnenprogramm auf euch.'
    },
    donation: {
      text: 'Dernau - ein ehemals malerisches Örtchen westlich von Bad Neuenahr-Ahrweiler mit rund 1700 Einwohnern - war eines der beliebtesten Ausflugsziele an der Ahr. Bekannt für seine historischen Weinkeller, die großen Weinbauflächen und den berühmten Rotweinwanderweg zog es jedes Jahr zahlreiche Touristen an.  Durch die Flutkatastrophe wurden nun nicht nur Häuser, Autos und Brücken zerstört, auch private und berufliche Existenzen liegen in Trümmern. Um das Ahrtal und Dernau wieder in seiner alten Schönheit erstrahlen zu lassen wird jede Hilfe benötigt und dafür brauchen wir euch! ',
      help: "Egal ob Privatperson oder Monheimer Unternehmerin oder Unternehmer, wir bitten euch, dass ihr euch an unserer Aktion “ Aahrr! Hilfe“  beteiligt. Durch Sach- oder finanzielle Hilfen, ausgefallene Dinge die man versteigern kann, what ever…",
      donation: 'Ihr könnt jederzeit Spenden! Auch wenn ihr an dem Abend nicht dabei sein könnt, würden wir uns freuen, wenn ihr den Spendentopf noch praller werden lasst.'
    },
    spirits: [
      {
        url: 'https://monshiners.de',
        title: 'MONSHINERS\' OBSTBRAND 20',
        text: 'Heiß begehrt und nach 21 Minuten ausverkauft: Das war die erste Abfüllung der Monshiners aus 2020! Jetzt werden die letzten Flaschen für den guten Zweck versteigert. Das Besondere: Die Seriennummer wurden durch 40789 und 4019 ersetzt.',
        src: require('@/assets/monshiners_bottle.png')
      },
      {
        url: 'https://monshiners.de',
        title: 'Rosebank 1991 Signatory Vintage 12 Jahre',
        text: 'Ein besonders rarer Tropfen der mittlerweile geschlossenen Rosebank Distillery in den schottischen Lowlands. Flasche Nr.272 von nur 467.',
        src: require('@/assets/signatory.png')
      },
      {
        url: 'https://simplykaschemm.de',
        title: 'DON PAPA SHERRY CASK',
        text: 'Simply Kaschemm versteigert einen besonders feinen Tropfen. Der Don Papa Sherry Cask reift zunächst für vier Jahre in Ex-Bourbonfässern aus amerikanischer Weißeiche und erhält anschließend für 18 Monate ein Finish in vier verschiedenen spanischen Sherryfässern. Auch hier wieder eine limitierte Edition.',
        src: require('@/assets/don_papa.png')
      },
    ],
    participants: [
      {
        url: 'https://monshiners.de',
        text: 'Obstbrände aus dem Monheimer Rheinbogen. Die schnellsten Treckerfahrer der Stadt. Geistreiche Trinker und Obstbauern aus Leidenschaft.',
        src: require('@/assets/participants/monshiners.jpg')
      },
      {
        url: 'https://simply-kaschemm.com/',
        text: 'Ausgewählte Spirituosen aus aller Welt von Liebhabern für Liebhaber. Und für die, die es werden wollen.',
        src: require('@/assets/participants/simply_kaschemm.jpg')
      }
    ],
    mighties: {
      src: require('@/assets/mighties_logo.jpg'),
      text: 'Die Mighties beehren uns und werden nicht irgendwelche Songs spielen. Aus 25 Songs könnt ihr die TOP 8 des Abends ersteigern. Umso mehr Geld für einen Song zusammenkommt, umso höher ist die Wahrscheinlichkeit, dass er gespielt wird!'
    },
  }),
};
</script>

<style lang="scss">
@import 'src/styles/variables.scss';

.source-sans-pro {
  font-family: Source Sans Pro, sans-serif;
  letter-spacing: 0.05em;
  font-weight: 900;
  word-break: normal;
}

.application {
  background-color: #ffff00;
}
</style>


