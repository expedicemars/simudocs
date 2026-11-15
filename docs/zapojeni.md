# Zapojení a zapnutí


1. Připrav si server a sitove prvky (2 routery a repeater).
2. Zapoj kabely do konektorů
    - podle možnosti připojení k místni síti:
        + je kabel = ethernet mistni site <---> port eth1 na serveru
        + není kabel = repeater <---> port eth1 na serveru
    - posadka lan = router ..... port wan <---> port eth2 na serveru
    - EMMC lan = router ..... port wan <---> port na pridavne eth karte v serveru (ten nahore)
    - Napájecí kabel do zdroje 1, popřípadě 1 a 2.
3. Zapni server tlačítkem vepředu.
4. Na předním displeji serveru zmackni prostřední tlačítko a jed uplne doprava. tam 
zmáčkni tlacitko hide all. tim smažeš všechny nedůležité chyby.
5. Pokud jsi připojený přes repeater, musíš mu nastavit přes aplikaci tplink IP passthru a připojení na wifi
6. odzkoušej funkčnost. Pokud to nefunguje a od zapnutí neuběhlo 10 minut, počkej!
