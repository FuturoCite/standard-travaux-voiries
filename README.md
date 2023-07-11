# Schéma des travaux de voiries
Ce schéma permet de modéliser les différents attributs des travaux de voiries 

## Contexte

Il existe un besoin d'harmonisation de la publication en open data de données essentielles produites par les administrations publiques wallonnes. En octobre 2022, plus de 660 jeux de données sont publiés sur le portail [Open Data Wallonie Bruxelles (ODWB)](https://www.odwb.be/explore/?sort=modified), qui sont très hétérogènes. 

Constatant la production de jeux de données disparates à l'échelle de la fédération Wallonie-Bruxelles, FuturoCité a réuni, dans le cadre d'un groupe de travail sollicité depuis mai 2021, une vingtaine de collectivités. La concertation de celles-ci a permis 1) d'identifier collectivement des jeux de données jugés prioritaires et 2) de s'accorder sur des spécifications des modèles de données. 
La standardisation de ces données prioritaires est en effet essentielle pour s'assurer de leur publication homogène et de faciliter leur exploitation (notamment leur agrégation) par les réutilisateurs. Elle facilitent l'exploitation des données publiées par les réutilisateurs (agrégation, consolidation et traitements automatiques).

## Construction du schéma de données 

Les membres du groupe de travail ont défini un schéma de données qui décrit le format des fichiers, les différents champs, les valeurs possibles… Ils se sont appuyés sur un état des lieux du patrimoine de données des collectivités wallonnes et sur une étude des modèles utilisés par des collectivités déjà productrices de ces données (notamment Liège et Namur), en prenant en compte les retours faits par les réutilisateurs de données. 

## Description du schéma

Un [gabarit au format tableur](https://github.com/FuturoCite/standard-travaux-voiries/blob/main/Schema_travaux_voiries_gabarit.xlsx) est également prévu pour faciliter la publication d'un jeu de données conforme au format du schéma.

Un exemple valide au format CSV est consultable [ici](https://github.com/FuturoCite/standard-travaux-voiries/blob/main/exemple-valide.csv).  

Le tableau ci-dessous donne un aperçu des champs du schéma.

<table>
  <tr>
   <td><strong>Nom</strong>
   </td>
   <td><strong>Remplissage obligatoire/optionnel</strong>
   </td>
   <td><strong>Description</strong>
   </td>
  </tr>
  <tr>
   <td>Identifiant unique du chantier 
     <br>(id)
   </td>
   <td>Obligatoire
   </td>
   <td>Ce champ contient un identifiant unique local. Le producteur de données le génère en associant le code INS de la commune dans laquelle se situe le chantier à un nombre. Ce champ permet d'éviter localement les doublons. Le code INS de la commune est accessible ici :<a href="https://statbel.fgov.be/fr/open-data/code-refnis"> https://statbel.fgov.be/fr/open-data/code-refnis</a>
   </td>
  </tr>
  <tr>
   <td>Nom 
     <br>(name)
   </td>
   <td>Obligatoire
   </td>
   <td>Ce champ renseigne le nom du chantier.
   </td>
  </tr>
  <tr>
   <td>Description 
     <br>(description)
   </td>
   <td>Optionnel
   </td>
   <td>Ce champ contient une description complète des travaux. Si le chantier suit ou est suivi d'autres travaux, cela peut-être précisé.
   </td>
  </tr>
  <tr>
   <td>Lien description chantier 
     <br>(description_url)
   </td>
   <td>Optionnel
   </td>
   <td>Si le chantier est documenté sur une page web, le producteur de données peut renseigner l'URL dans ce champ.
   </td>
  </tr>
  <tr>
   <td>Nom de la commune 
     <br>(municipality)
   </td>
   <td>Obligatoire
   </td>
   <td>Le champ indique le nom de la commune dans laquelle se déroule les travaux. Le nom de la commune provient de la base de données BeST Address : https://opendata.bosa.be/index.fr.html ou de la liste des codes INS : https://statbel.fgov.be/fr/open-data/code-refnis
   </td>
  </tr>
  <tr>
   <td>Code INS 
     <br>(ins_code)
   </td>
   <td>Obligatoire
   </td>
   <td>Ce champ contient le code INS de la commune où se situe le chantier. Il est accessible ici :<a href="https://statbel.fgov.be/fr/open-data/code-refnis"> https://statbel.fgov.be/fr/open-data/code-refnis</a>
   </td>
  </tr>
  <tr>
   <td>Partie de commune 
     <br>(zone_address)
   </td>
   <td>Optionnel
   </td>
   <td>Ce champ contient le nom de la partie de commune où se situe le chantier, conforme à l'appelation dans StatBel :<a href="https://statbel.fgov.be/fr/propos-de-statbel/methodologie/classifications/geographie"> https://statbel.fgov.be/fr/propos-de-statbel/methodologie/classifications/geographie</a>
   </td>
  </tr>
  <tr>
   <td>Code INS de la partie de commune 
     <br>(ins_zone_address)
   </td>
   <td>Optionnel
   </td>
   <td>Ce champ contient le code INS de la partie de commune où se situe le chantier. La découpe géographique de StatBel Level 5 (NIS6) liste ces codes :<a href="https://statbel.fgov.be/fr/propos-de-statbel/methodologie/classifications/geographie"> https://statbel.fgov.be/fr/propos-de-statbel/methodologie/classifications/geographie</a>
   </td>
  </tr>
  <tr>
   <td>Nom de rue 
     <br>(street_name)
   </td>
   <td>Obligatoire
   </td>
   <td>Ce champ contient le nom de la voirie concernée par les travaux.
   </td>
  </tr>
  <tr>
   <td>Code rue BeSTAddress 
     <br>(street_number)
   </td>
   <td>Obligatoire
   </td>
   <td>Ce champ contient le code de la voirie où se situent les travaux dans la base de données BeSTAdress (ou de la voirie la plus proche) :<a href="https://opendata.bosa.be/index.fr.html"> https://opendata.bosa.be/index.fr.html</a>
   </td>
  </tr>
  <tr>
   <td>Code rue national 
     <br>(street_number_rrn)
   </td>
   <td>Optionnel
   </td>
   <td>Code de la voirie où se situe le chantier dans le registre national (ou de la voirie la plus proche).
   </td>
  </tr>
  <tr>
   <td>Localisation 
     <br>(location)
   </td>
   <td>Optionnel
   </td>
   <td>Ce champ précise l'endroit de la voirie où se trouve le chantier.
   </td>
  </tr>
  <tr>
   <td>Type de travaux 
     <br>(roadworks_type)
   </td>
   <td>Obligatoire
   </td>
   <td>Le champ précise le type de travaux de voirie. Les valeurs possibles sont : Aménagement de voiries (création d'un trottoir, installation d'un ralentisseur, ...) ; Impétrant (installation du gaz, remplacement des égouts, …) ; Réfection de voiries (remplacement du revêtement, réparation d'un nid de poule, entretien des trottoirs, ...) ; Création de voiries ; Autre
   </td>
  </tr>
  <tr>
   <td>Description du type de travaux 
     <br>(roadworks_type_description)
   </td>
   <td>Optionnel (recommandé)
   </td>
   <td>Ce champ est recommandé. Il précise la nature des travaux.
   </td>
  </tr>
  <tr>
   <td>Statut du chantier 
     <br>(status)
   </td>
   <td>Obligatoire
   </td>
   <td>Ce champ informe sur le statut du chantier. Ce champ doit être mis à jour au moment du changement de statut (début ou fin des travaux). Les valeurs possibles sont : Planifié ; En cours ; Terminé
   </td>
  </tr>
  <tr>
   <td>Année 
     <br>(year)
   </td>
   <td>Obligatoire
   </td>
   <td>Ce champ renseigne sur l'année de début du chantée.
<p>
Pour un chantier planifié, renseigner l'année de début prévue. Pour un chantier en cours ou terminé, indiquer l'année de début effective.
<p>
Ce champ doit être mis à jour lorsque la date de début du chantier évolue.
   </td>
  </tr>
  <tr>
   <td>Date de début 
     <br>(start_date)
   </td>
   <td>Obligatoire
   </td>
   <td>Ce champ renseigne la date exacte de début du chantier. Pour un chantier planifié : date de début prévue. Pour un chantier en cours ou terminé : date de début effective.
<p>
Le champ respecte le format ISO 8601 : année-mois-jour (YYYY-MM-DD).
<p>
Il doit être mis à jour lorsque la date de début du chantier évolue.
   </td>
  </tr>
  <tr>
   <td>Date de fin 
     <br>(end_date)
   </td>
   <td>Obligatoire
   </td>
   <td>Ce champ indique la date de fin du chantier. Pour un chantier planifié ou en cours : date de fin prévue. Pour un chantier terminé : date de fin effective.
<p>
Le champ respecte le format ISO 8601 : année-mois-jour 
  <br>(YYYY-MM-DD).
<p>
Ce champ doit être mis à jour lorsque la date de fin du chantier évolue.
   </td>
  </tr>
  <tr>
   <td>Geométrie 
     <br>(geometry)
   </td>
   <td>Optionnel (recommandé)
   </td>
   <td>Ce champ est recommandé. Il indique la zone du chantier grâce à une liste de coordonnées. Cette liste est générée à partir d'un fichier GPX.
   </td>
  </tr>
  <tr>
   <td>Superficie du chantier 
     <br>(site_area)
   </td>
   <td>Optionnel
   </td>
   <td>Ce champ indique la superficie du chantier en mètres carrés.
   </td>
  </tr>
  <tr>
   <td>Longueur de voirie en chantier 
     <br>(length)
   </td>
   <td>Optionnel
   </td>
   <td>Ce champ indique la longueur de la voirie concernée par le chantier en mètres.
   </td>
  </tr>
  <tr>
   <td>Validé par les autorités 
     <br>(validated_by_authorities)
   </td>
   <td>Optionnel
   </td>
   <td>Ce champ précise si le chantier a été validé par les autorités (valeur 'true') ou non (valeur 'false'). Si non applicable : ne pas renseigner ce champ.
   </td>
  </tr>
  <tr>
   <td>Impacts du chantier 
     <br>(impact)
   </td>
   <td>Optionnel
   </td>
   <td>Ce champ décrit les impacts prévus par le chantier (mobilité, environnement, bruit, …)
   </td>
  </tr>
  <tr>
   <td>Adaptations de la circulation 
     <br>(traffic_adaptation)
   </td>
   <td>Optionnel (recommandé)
   </td>
   <td>Ce champ est recommandé. Il indique l'éventuel dispositif modifiant la circulation pendant la durée du chantier. Les valeurs possibles sont (un choix) : Sens unique ; Sens unique limité ; Réduction du nombre de bandes ; Circulation alternée ; Voie fermée ; Vitesse réduite ; Limitation selon le gabarit du véhicule ; Pas de modification
   </td>
  </tr>
  <tr>
   <td>Gestionnaire du chantier 
     <br>(provider)
   </td>
   <td>Obligatoire
   </td>
   <td>Ce champ indique le nom du commanditaire (public ou privé) du chantier.
   </td>
  </tr>
  <tr>
   <td>Responsable de la signalisation 
     <br>(signage_manager)
   </td>
   <td>Optionnel (recommandé)
   </td>
   <td>Ce champ est recommandé. Il indique le nom du responsable de la signalisation du chantier.
   </td>
  </tr>
  <tr>
   <td>Entrepreneur 
     <br>(contractor)
   </td>
   <td>Optionnel (recommandé)
   </td>
   <td>Ce champ est recommandé. Il indique le nom de l'entrepreneur responsable du chantier
   </td>
  </tr>
  <tr>
   <td>Budget previsionnel 
     <br>(projected_budget)
   </td>
   <td>Optionnel (recommandé)
   </td>
   <td>Ce champ est recommandé. Il indique le budget prévisionnel du chantier exprimé en euros TVAC.
   </td>
  </tr>
  <tr>
   <td>Montant effectif 
     <br>(effective_amount)
   </td>
   <td>Optionnel (recommandé)
   </td>
   <td>Ce champ est recommandé. Il indique le montant effectif du chantier exprimé en euros TVAC.
   </td>
  </tr>
  <tr>
   <td>Date de création de la donnée 
     <br>(created_date)
   </td>
   <td>Optionnel (recommandé)
   </td>
   <td>Ce champ indique la date de création de la donnée dans le jeu. Il respecte le format ISO 8601 : année-mois-jour (YYYY-MM-DD)
   </td>
  </tr>
  <tr>
   <td>Date de dernière modification de la donnée 
     <br>(last_modified_date)
   </td>
   <td>Optionnel (recommandé)
   </td>
   <td>Ce champ indique la date de la dernière modification de la donnée dans le jeu. Il respecte le format ISO 8601 : année-mois-jour (YYYY-MM-DD).
   </td>
  </tr>
</table>

## Format de fichier 

Le format de fichier retenu pour la publication des données est le CSV (Comma Separated Values, valeurs séparées par des virgules).

Les fichiers doivent, sauf exception et autant que possible, respecter les règles de formatage suivantes :

* l’encodage des caractères est UTF-8,
* le séparateur des colonnes est la virgule,
* le séparateur des nombres décimaux est le point,
* le séparateur de valeurs multiples dans un champ est le point-virgule,
* si un champ contient une virgule, il doit être entouré de guillemets doubles,
* chaque ligne doit avoir le même nombre de champs,
* le type MIME ou Content-Type est text/csv.

### Recommandations pour le nommage des fichiers 

Les fichiers doivent, sauf exception et autant que possible, respecter les règles de nommage suivantes :

* YYYY-MM-DD : Date de création du fichier
* idProducteur : code INS unique de la commune pour identifier le producteur
* travaux-voiries : nom du fichier, en minuscules non accentuées
* territoire : Nom du territoire concerné, non accentué (exemple : Liege)
* extension : Si les règles de formatage sont respectées, l'extension est .csv

Exemple : 2022-10-25_62063_travaux-voiries_Liege.csv

### Recommandations pour la mise en conformité 

Ces conseils reprennent ceux des schémas standards de données français publié par [l'initiative de data.gouv.fr](https://schema.data.gouv.fr/).

Les fichiers doivent comporter :

* Toutes les colonnes, y compris celles dont les cellules ne sont pas renseignées, dans le bon ordre, et avec des en-têtes correctement nommées sur la première ligne (nom correspondant strictement au schéma)
* Autant de lignes que nécessaire comprenant des cellules dont les valeurs peuvent être obligatoires (elles doivent être impérativement renseignées) ou optionnelles (elles sont seulement recommandées ou soumises à condition de disponibilité / pertinence)
