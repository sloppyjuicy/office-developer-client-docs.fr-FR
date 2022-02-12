---
title: À propos de la prise en charge InfoPath pour les technologies XML
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 074181a2-3a75-824c-049d-549aabff0f9f
description: Microsoft InfoPath est un outil hybride qui combine le meilleur d’une expérience d’édition de documents traditionnelle, telle qu’un traitement de texte ou une application de messagerie, avec les fonctionnalités rigoureuses de capture de données d’un package de formulaires. Cet article décrit les problèmes qu'InfoPath est censé résoudre, et détaille les principes de conception et les standards XML que cette solution utilise.
ms.openlocfilehash: f2d83157199296642cf908dd2cd68c6c16c723a5
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62782828"
---
# <a name="about-infopath-support-for-xml-technologies"></a>À propos de la prise en charge InfoPath pour les technologies XML

Microsoft InfoPath est un outil hybride qui combine le meilleur d’une expérience d’édition de documents traditionnelle, telle qu’un traitement de texte ou une application de messagerie, avec les fonctionnalités rigoureuses de capture de données d’un package de formulaires. Cet article décrit les problèmes qu'InfoPath est censé résoudre, et détaille les principes de conception et les standards XML que cette solution utilise.
  
## <a name="introduction"></a>Introduction

InfoPath est un outil de création XML de haut niveau qui permet à tous les utilisateurs finaux de créer des documents XML appartenant à un schéma XML personnalisé. Lorsque l'utilisateur édite un document XML, les modifications apportées au document sont contrôlées par le schéma XML.
  
L'utilisateur interagit avec le document XML par le biais d'une vue enrichie et mise en forme, affichée en appliquant une feuille de style XSLT au document. Les nœuds terminaux et les valeurs d'attribut du document XML sont affichés sous forme de champ (par exemple une zone de texte ou une case à cocher) et les hiérarchies de nœuds sont rendues sous forme de groupes de champs.
  
InfoPath permet d'éditer les données XML de façon validée et structurée, en affichant les actions d'édition valides pour le champ ou le groupe de champs sélectionné. L'édition structurée offre aux utilisateurs la possibilité d'ajouter et de supprimer des éléments et attributs XML valides par le biais de groupes de champs affichés dans des vues dynamiques enrichies, sans afficher ces éléments et attributs.
  
En matière de collecte de données, InfoPath résout un problème impossible à résoudre avant la naissance du langage XML : en fournissant des formulaires évolutifs, capables d'accueillir d'autres groupes de champs utilisant le modèle de données hiérarchique du langage XML, InfoPath associe l'immense flexibilité des applications de traitement de texte aux fonctions rigoureuses de validation offertes par les applications de gestion de formulaires. Les transformations XSLT complexes font partie intégrante de cette solution, qui offre des vues dynamiques et simples d'utilisation des données XML.
  
## <a name="limitations-of-traditional-forms-and-documents-for-gathering-data"></a>Limites des formulaires et documents conventionnels en matière de collecte de données

Lors de la collecte de données d’entreprise, les utilisateurs souhaitent en général bénéficier d’une flexibilité plus importante que celle offerte par les formulaires statiques, tout en profitant de fonctions d’édition structurée et de validation plus sophistiquées que celles proposées par les applications de traitement de texte.
  
Les formulaires conventionnels sont statiques et limités en longueur. Le nombre de lignes extensibles est fixe et ils ne peuvent pas être étendus pendant le remplissage du formulaire. En outre, leur utilisation est complexe, car ils ne disposent pas de fonctions d'édition enrichie. Bien souvent, l'utilisateur doit fournir toutes les informations simultanément.
  
De leur côté, les documents conventionnels créés à l'aide d'une application de traitement de texte permettent à l'utilisateur d'ajouter et de supprimer du contenu à sa guise, mais ils lui laissent presque trop de marge de manœuvre, dans le sens où il n'est pas obligé de saisir des informations complètes, structurées et valides. Les champs définis dans le document font rarement l'objet d'une véritable validation des valeurs et des types de données. Les libellés associés aux données des champs sont insuffisants pour permettre de faire facilement référence aux données et de les réutiliser automatiquement. Au lieu d'être structuré, le format des données est libre. Enfin, vous ne pouvez pas regrouper des informations, par exemple appliquer un libellé « Adresse » à un groupe associé aux champs « Rue », « Ville » et « État ».
  
Des outils d’édition aussi flexibles que structurés s’avèrent donc nécessaires. Cependant, avant l’arrivée du langage XML, ce type de technologie n’était pas disponible. Entre temps, les développeurs ont été amenés à créer des applications personnalisées nécessitant un codage sophistiqué. Ces applications sont coûteuses et difficiles à modifier, et la validation nécessite un codage personnalisé. Il est bien souvent nécessaire de former les utilisateurs finaux et il s’avère difficile de réutiliser les données obtenues dans d’autres processus d’entreprise.
  
## <a name="providing-structured-editing-by-displaying-xml-data-as-field-groups"></a>Accès à l’édition structurée grâce à l’affichage de données XML sous forme de groupes de champs

Sur le plan de la conception technique, l’une des principales difficultés fut de trouver comment créer une interface simple d’utilisation permettant d’ajouter et de supprimer des éléments et attributs XML sans les afficher, tout en conservant une arborescence DOM conforme au schéma XML personnalisé défini. Une telle interface utilisateur devait donc permettre d’éditer facilement l’arborescence DOM, notamment en insérant des sous-arborescences facultatives, en remplaçant les sous-arborescences disponibles et en étendant les sous-arborescences existantes.
  
Pour fournir une interface simple d'utilisation, une sous-arborescence DOM s'affiche sous la forme d'un groupe de champs (ou section). Un groupe de champs est un groupe de contrôles d'interface utilisateur (zones de texte, listes déroulantes, etc.) qui joue le rôle d'interface simple permettant à l'utilisateur de visualiser et d'éditer des données XML hiérarchiques. À l'instar des sous-arborescences DOM, qui peuvent contenir d'autres sous-arborescences et être facultatives ou extensibles, un groupe de champs peut contenir d'autres groupes de champs et être facultatif ou extensible. Une sous-arborescence est ajoutée à l’arborescence DOM lorsque l’utilisateur place le pointeur de la souris sur un groupe de champs, clique sur le menu déroulant qui apparaît sur le groupe de champs, puis sélectionne **Insérer \<field group name\>**.
  
InfoPath permet d'éditer les données XML de façon structurée en utilisant le schéma XML spécifié pour encadrer et guider l'édition. Le schéma détermine notamment si les commandes **Insérer** et **Supprimer** doivent ou non s'afficher dans le menu déroulant d'un groupe de champs. Ce schéma est également utilisé pour la validation. Pour permettre l'édition d'un document XML pour lequel il n'existe pas de schéma, InfoPath peut générer un schéma à partir du document XML. 
  
## <a name="providing-easy-to-use-views-of-xml-data-by-using-xslt-transformations"></a>Accès à des vues de données XML simples d’utilisation à l’aide de transformations XSLT

Une des autres difficultés techniques à résoudre consistait à trouver un moyen d'organiser le contenu des vues de l'interface utilisateur sans forcément reprendre la structure des données XML. Pour présenter les données de façon claire pour l'utilisateur et lui permettre de les lire et de les éditer facilement, le concepteur doit pouvoir afficher les données dans un ordre différent de celui dans lequel elles apparaissent dans l'arborescence de données DOM, ignorer certaines données figurant dans une vue, réorganiser des nœuds d'arborescence de données adjacents dans des vues séparées et regrouper dans une même vue des données issues de différentes sections de l'arborescence.
  
L'ordre et la structure du contenu des vues doivent par conséquent être indépendants de l'ordre et de la structure des nœuds de l'arborescence DOM. Cette indépendance structurelle en termes de présentation et de données nécessite une liaison ou un mappage complexe et dynamique entre les champs groupés dans les vues et les nœuds de l'arborescence DOM.
  
Pour créer ce mappage complexe entre les vues et les données, InfoPath s'appuie de façon importante sur le langage XSLT (XSL Transformations). XSLT est un puissant langage de feuille de style qui prend en charge les transformations XSLT complexes et les vues enrichies, et qui permet de présenter le contenu de façon dynamique et flexible. Un fichier XSLT distinct est associé à chaque vue. L'utilisation de feuilles de style est désormais une approche courante et bien établie dans les outils de création SGML et XML, et XSLT est le standard W3C des feuilles de style utilisées dans le cadre de ces transformations complexes.
  
Pour éviter d'exécuter entièrement la transformation XSLT chaque fois que l'utilisateur modifie la structure d'une sous-arborescence du DOM, des algorithmes déterminent quelle partie de la vue doit être actualisée. Ainsi, seule la partie concernée de la feuille de style XSLT est appliquée et la partie en question est actualisée dans la vue.
  
## <a name="how-xml-standards-are-used-when-editing-a-form"></a>Utilisation des standards XML lors de l’édition d’un formulaire

InfoPath s'appuie entièrement sur les standards XML suivants :
  
- Extensible Markup Language (XML) 1.0 Second Edition
    
- Namespaces in XML
    
- XML Path Language (XPath) 1.0
    
- XML Schema (XSD) 1.0 Part 1: Structures, and Part 2: Datatypes
    
- Extensible Stylesheet Language Transformations (XSLT) 1.0
    
- Extensible Hypertext Markup Language (XHTML) 1.0
    
- Cascading Style Sheets (CSS)
    
- Document Object Model (DOM) 1.0
    
- XML Digital Signatures (XML DSig)
    
- Simple Object Access Protocol (SOAP) 1.1
    
- Web Services Description Language (WSDL) 1.1
    
- Universal Description, Discovery, and Integration (UDDI) 1.0
    
Par exemple, InfoPath exploite et génère des fichiers XML, XSLT et XSD standard réutilisables dans différents processus d'entreprise. InfoPath utilise MSXML, SOAP Toolkit et l'espace de noms .NET System.XML pour prendre en charge ces standards, et prend intégralement en charge les services Web XML.
  
La figure 1 illustre le menu déroulant contextuel d'un groupe de champs **customer**, qui permet à l'utilisateur d'ajouter un autre groupe de champs **customer**, de supprimer ce groupe de champs **customer**, d'insérer une ligne **item** dans la table des achats de ce groupe de champs, ou encore d'insérer un groupe de champs **actions** facultatif au sein de ce groupe de champs. Le lien **Cliquez ici** offre un autre moyen d'insérer le groupe de champs **actions**. Un menu déroulant raccourci s'affiche sur chaque ligne d'achat. 
  
1. Dans InfoPath, l'utilisateur crée un document XML à partir d'un modèle de formulaire InfoPath ou ouvre un document XML existant basé sur un modèle de formulaire. Le document XML, qui peut utiliser des espaces de noms XML, est un fichier de données XML contenant une référence au modèle de formulaire. 
    
    Un modèle de formulaire est un ensemble de fichiers permettant d'éditer des documents XML de façon structurée, conformément à un schéma XML personnalisé. Les fichiers composant ce modèle de formulaire peuvent être regroupés sous forme de fichiers individuels dans un dossier standard ou sous forme de fichiers stockés dans un dossier CAB. Dans les deux cas, il s'agit de fichiers XML standard et de fichiers de prise en charge facultatifs (assemblys de code managé, par exemple).
    
2. Si le document XML est signé numériquement par le biais d'une signature XML, InfoPath vérifie que le fichier XML est cohérent avant de l'ouvrir.
    
3. InfoPath crée une arborescence de données DOM du document XML en mémoire.
    
4. Les transformations XSLT sont appliquées à l'arborescence DOM et génèrent des vues présentant de façon adaptée le document à l'utilisateur. Les éléments figurant au début du document XML peuvent très bien être affichés en bas de la vue et dans un autre ordre dans une autre vue. Les vues se composent de conteneurs d'interface utilisateur, par exemple de sections contenant du texte et des contrôles (zones de texte, zones de texte enrichies, sélecteurs de dates, listes déroulantes, etc.). Les conteneurs peuvent en outre contenir d'autres conteneurs.
    
5. La transformation XSLT produit une sortie XHTML et une feuille de style CSS est ensuite utilisée pour contrôler la présentation du contenu XHTML.
    
6. Si le schéma XML autorise l'ajout de nœuds à un nœud de l'arborescence de données, le champ ou le groupe de champs mappé au nœud dispose d'un menu déroulant qui permet à l'utilisateur d'ajouter ou de supprimer des groupes de champs. L'utilisateur édite le document en y ajoutant un groupe de champs extensible ou facultatif, en y saisissant une valeur, en y sélectionnant une option ou encore en y saisissant du texte enrichi. Si un nœud de schéma XML est associé au schéma XHTML, InfoPath présente une interface utilisateur permettant de créer du texte enrichi. Lorsque l'utilisateur saisit du texte enrichi, le contenu XHTML est créé en tant que sous-arborescence du DOM.
    
7. La validité de l'arborescence DOM est assurée en permanence. Lorsque l'utilisateur édite le document XML, les modifications sont validées par rapport au schéma XML associé. Les tentatives de modification de la structure du DOM et des valeurs du nœud terminal sont validées par rapport au schéma XML, afin de garantir la validité des types et valeurs de données. Si les tentatives de modification ne sont pas valides, une boîte de dialogue de validation s'affiche et les modifications ne sont pas appliquées à l'arborescence DOM. Si les modifications sont valides, l'arborescence DOM est mise à jour.
    
8. La partie modifiée de la vue est actualisée et seules les parties requises de la feuille de style XSLT sont appliquées à l'arborescence DOM.
    
9. L'utilisateur peut enregistrer le document XML ou le transmettre par le biais du protocole HTTP standard ou du protocole SOAP. En revanche, il n'est pas autorisé à transmettre le document s'il n'est pas conforme au schéma XML.
    
## <a name="how-xml-standards-are-used-when-designing-a-form"></a>Utilisation des standards XML lors de la conception d’un formulaire

Vous pouvez concevoir un formulaire à partir d'un schéma XML existant, en vous connectant à un service Web XML ou à une base de données et en obtenant son schéma XML, ou encore en générant automatiquement un schéma à partir d'un nouveau formulaire ou d'un fichier de données XML. Ces différents scénarios sont décrits dans les procédures ci-dessous. La figure 3 illustre l'interface utilisateur de base permettant de concevoir un modèle de formulaire.
  
1. Créez un formulaire dans InfoPath Designer en sélectionnant le modèle de formulaire **Fichier ou schéma XML**, puis sélectionnez un fichier de schéma XML existant comme source de données. Celui-ci est chargé dans le volet Office et affiché en tant que contrôle d'arborescence. 
    
2. Utilisez les outils de conception pour définir la présentation des contrôles de l'interface utilisateur, tels que les lignes et le style d'arrière-plan, dans une ou plusieurs vues. Cette opération génère une partie des éléments XSLT. Les vues XSLT et le schéma XML sont automatiquement associés au modèle de formulaire.
    
3. Mappez les éléments du schéma XML aux contrôles d'interface utilisateur figurant dans les vues à l'aide d'opérations de glisser-déplacer. InfoPath vous aide à choisir les contrôles adaptés aux éléments du schéma XML, en fonction du type d'élément de schéma. Par exemple, si le type de données XML est date, InfoPath suggère un contrôle de sélecteur de dates. En fonction des choix disponibles dans le schéma XML, InfoPath insère des groupes de champs facultatifs ou extensibles. Le fait de mapper les éléments du schéma XML aux contrôles d'interface utilisateur génère la structure XSLT.
    
4. Enregistrez le modèle de formulaire. Vous pouvez enregistrer les fichiers qui composent ce modèle sous forme de fichiers individuels dans un dossier standard ou sous forme de fichiers stockés dans un dossier CAB. Dans les deux cas, il s'agit de fichiers XML standard. L'utilisateur peut dès à présent utiliser le modèle de formulaire.
    
Un modèle de formulaire contient toutes les informations sémantiques permettant l'édition structurée d'un formulaire ouvert dans InfoPath. Il inclut un fichier manifeste, les fichiers XSLT définissant les vues, les informations nécessaires pour valider les données, ainsi qu'un ID de ressource facultatif pour un service Web XML.
  
Le manifeste, également appelé fichier de définition de formulaire, est le noyau commun et le point d'entrée de tous les fichiers composant le modèle de formulaire. Le manifeste contient des références aux autres fichiers du modèle de formulaire, ainsi que les informations nécessaires pour valider les données et permettre l'édition structurée. Les informations de validation du schéma XML sont adaptées à l'interface utilisateur obtenue et ajoutées au fichier manifeste. Par exemple, si le schéma autorise l'insertion de plusieurs éléments facultatifs dans une sous-arborescence spécifique, vous pouvez concevoir l'interface utilisateur de telle sorte que plusieurs éléments facultatifs soient ajoutés lorsque l'utilisateur réalise une opération dans l'interface. Cette personnalisation est indispensable pour faciliter le travail de l'utilisateur final. 
  
Vous pouvez également concevoir un formulaire en utilisant un service Web XML existant pour créer le schéma XML. Pour ce faire, procédez comme suit :
  
1. Utilisez un service UDDI pour rechercher les services Web concernés.
    
2. Sélectionnez le service Web à utiliser. InfoPath lit le fichier WSDL associé au service Web et identifie le schéma XML à utiliser.
    
3. Ouvrez le schéma XML pour le charger.
    
4. Configurez la disposition des contrôles d'interface utilisateur et associez-les aux éléments et attributs du schéma XML.
    
5. Définissez le mode de transmission du document XML au service Web utilisant SOAP.
    
Si vous souhaitez concevoir intégralement un nouveau formulaire et générer automatiquement le schéma XML, procédez comme suit :
  
1. Dans l'onglet **Fichier**, sélectionnez le modèle de formulaire **Formulaire vierge** ou **Formulaire vierge (InfoPath Filler)**, puis cliquez sur **Créer un formulaire**.
    
2. Dans l'onglet **Accueil**, cliquez sur la flèche en bas à droite du groupe **Commandes** pour afficher le volet Office **Commandes** et vérifiez que la case à cocher **Créer automatiquement la source de données** est activée. Cette case à cocher est activée par défaut. 
    
3. Configurez la disposition des contrôles d'interface utilisateur. À mesure que vous configurez leur disposition, InfoPath crée automatiquement le schéma XML et mappe ses éléments et attributs aux contrôles d'interface utilisateur.
    
Pour concevoir un formulaire à partir d'un fichier de données XML bien formé, procédez comme suit :
  
1. Dans l'onglet **Fichier**, sélectionnez le modèle de formulaire **Fichier ou schéma XML**, puis cliquez sur **Créer un formulaire**.
    
2. Dans l' **Assistant Source de données**, puis sélectionnez le fichier XML comme source de données. Un schéma XML basé sur le fichier de données XML est créé automatiquement.
    
3. Configurez la disposition des contrôles d'interface utilisateur comme indiqué ci-dessus.
    
## <a name="designed-as-an-ideal-client-for-web-services"></a>Le client idéal des services Web

Les services Web sont désormais pris en charge par de nombreux acteurs du monde informatique. Bon nombre de systèmes principaux ou intermédiaires peuvent être configurés pour communiquer par le biais de standards de services Web tels que SOAP, UDDI et WSDL. Ainsi, de nombreux systèmes de bases de données ou de flux de travail, et de nombreuses solutions ERP (Enterprise Resource Planning) et CRM (Customer Relationship Management), mais aussi d'autres types de systèmes, sont désormais compatibles avec les services Web. InfoPath est devenue l'interface utilisateur idéale pour l'affichage et l'édition des données XML transmises par le biais de services Web. La figure 4 illustre le concept de prise en charge intégrée des services Web XML.
  
InfoPath s'intègre parfaitement à la souplesse du modèle des services Web, dans lequel les données transitent entre des ordinateurs sous la forme de documents XML intégraux. Ce modèle de communication plutôt sommaire est bien adapté à la nature asynchrone du Web. En tant qu'outil de création de documents XML de haut niveau, InfoPath prend en charge le codage SOAP document/littéral en lieu et place du codage SOAP RPC (Remote Procedure Call). InfoPath est ainsi un client idéal pour les services Web, car il peut lire en mode natif le schéma XML spécifié dans un message SOAP, puis créer une interface utilisateur à partir de ce schéma. Les utilisateurs finaux peuvent par conséquent afficher et éditer les documents XML générés ou reçus par le service Web correspondant. InfoPath prend également en charge les DataSets ADO.NET avec suivi des modifications.
  
## <a name="terminology"></a>Terminologie

|||
|:-----|:-----|
|**Groupe de champs :** <br/> |Section, section extensible, section facultative ou tableau extensible. Les sections et les tableaux extensibles sont des contrôles de formulaire contenant d’autres contrôles et qui s’étendent en fonction des besoins. Les utilisateurs peuvent insérer plusieurs sections ou lignes lorsqu’ils remplissent le formulaire. |
|**Arborescence DOM :** <br/> |Structure de la source de données du formulaire. En particulier, la collection de champs et de groupes qui définissent et stockent les données d’un formulaire InfoPath. |
   
## <a name="conclusion"></a>Conclusion

InfoPath utilise des standards XML ouverts pour offrir aux utilisateurs des fonctions d'édition XML aussi flexibles que structurées en vue de collecter des données. Pour que cette interface utilisateur soit simple d'utilisation et permette d'afficher et d'éditer les données hiérarchiques XML, les groupes de champs imbriqués contenant des contrôles d'interface utilisateur sont mappés à l'arborescence DOM. Les transformations XSLT permettent d'organiser le contenu des vues de l'interface utilisateur différemment de la structure des données XML.
  
InfoPath offre plus de flexibilité que les formulaires statiques, tout en proposant des fonctions d'édition et de validation plus structurées que celles des applications de traitement de texte. Au final, l'utilisateur dispose d'un outil hybride qui associe les meilleures fonctions conventionnelles d'édition de documents aux fonctions rigoureuses de collecte de données des outils de gestion de formulaires. N'importe quel utilisateur peut ainsi créer des documents XML valides appartenant à un schéma XML personnalisé. La prise en charge intégrée des services Web permet de définir facilement des vues afin d'éditer des documents XML conformes à un schéma de services Web.
  

