# Barcelona · Un autre horizon

Carnet interactif rétrospectif, construit d'après les échanges de préparation du voyage du **24 au 28 avril 2026**.

**Publication attendue :** https://nogues.app/visite-barcelone/

## Contenu et véracité

Les réservations explicitement connues sont :
- 24 avril : nuit au Perthus ;
- 25 avril : nuit au Sallés Hotel Pere IV, **billet Moco 15 h, billet Musée Picasso 16 h 30** ;
- 26 avril : hébergement Calendula Hotel & Apartament à Sant Feliu ;
- 27 avril : nuit Les Elmes, Banyuls-sur-Mer.

Fondation Miró, Montjuïc, promenades dans Barcelone, Camí de Ronda et Tour Madeloc : activités souhaitées ou proposées dans la conversation ; **leur réalisation n'est pas documentée**. Les marqueurs et le carnet distinguent ces deux états. Les localisations sont indicatives et certaines coordonnées d'hôtels approximatives. Les traits cartographiques sont des **liaisons schématiques**, jamais des itinéraires GPS.

## Stack

HTML5, CSS responsive, JavaScript natif, Leaflet 1.9.4 embarqué localement, OpenStreetMap, design system commun \`/ds/v1/\`, workflow GitHub Actions + lftp / SFTP.

## Déploiement

Depuis \`main\`, le workflow publie **uniquement** \`www/visite-barcelone/\` vers \`www/visite-barcelone/\` sur OVHcloud, sans suppression distante.

Secrets requis : \`OVH_SFTP_HOST\`, \`OVH_SFTP_USER\`, \`OVH_SFTP_PASSWORD\`, **\`OVH_SFTP_HOST_FINGERPRINT\`** (empreinte hôte SSH validée séparément). Le quatrième secret est indispensable à la sécurité ; aucune désactivation silencieuse de la vérification de l'hôte.

L'accès au contenu n'est **pas** protégé par mot de passe. \`noindex\` empêche l'indexation volontaire, mais ne rend pas l'URL privée.

## Confidentialité / médias

Aucun traceur d'audience et aucune clé API. Fond de carte tiers OpenStreetMap, image Commons illustrative, jamais présentée comme photographie du voyage. Visuel Open Graph original SVG. Image de partage source à exporter si besoin.

## Vérification

Tester la carte en plusieurs largeurs, les tuiles, les popups, le changement de jour, le clavier, les CSS clair/sombre, les liens, la réponse HTTP de production et les journaux GitHub Actions. Le résultat d'un commit/merge ne suffit pas à prouver la publication.
