---
title: Glossaire des objets de données ActiveX (ADO)
TOCTitle: ADO Glossary
ms:assetid: 40f00876-7525-4117-8f57-f3d87c54be99
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249184(v=office.15)
ms:contentKeyID: 48544438
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7ecb6208a8c970f037cb0ac699c947544eb8f547
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284833"
---
# <a name="ado-glossary"></a>Glossaire ADO

**S’applique à** : Access 2013, Office 2013

## <a name="a"></a>A

**URL absolue**

URL complète qui spécifie l'emplacement d'une ressource qui réside sur Internet ou un intranet. Voir aussi **URL** et **URL relative**.

**Contrôle ActiveX**

Composant COM à inscription automatique, qui possède souvent un élément visuel au moment de la conception ou au moment de l'exécution. Les contrôles ActiveX ont également la possibilité de communiquer avec un conteneur de documents actifs, tel que Microsoft Internet Explorer.

**ADISAPI (Advanced Data Internet Server Application Programming Interface)**

Une DLL ISAPI qui fournit l'analyse, le contrôle d'automatisation, le marshaling du **jeu d'enregistrements** et le Packaging MIME. Le composant ADISAPI fonctionne via l'API fournie par Internet Information Services (IIS). Voir aussi **ISAPI**.

**fonction d’agrégation**

Dans une requête, fonction telle que COUNT, AVG ou STDEV qui calcule une valeur à l'aide de toutes les lignes d'une colonne d'un tableau. Lors de l'écriture d'expressions et de la programmation, vous pouvez utiliser des fonctions d'agrégation SQL (notamment les trois ci-dessus) et des fonctions d'agrégation de domaine pour déterminer diverses statistiques.

**alias**

Un autre nom que vous attribuez à une colonne ou une expression dans une instruction SQL SELECT, souvent plus court ou plus significatif. Par exemple, BobSales est l'alias dans l'instruction SELECT suivante: "SELECT WR-Sales As BobSales from SalesDB". Un alias peut être utilisé pour affecter dynamiquement des colonnes à des liaisons de contrôle sur l'objet **DataControl** .

**thread cloisonné**

Modèle de thread COM où tous les appels vers un objet se produisent sur un seul thread. Dans le thread cloisonné, COM synchronise et marshale les appels. Voir aussi **com**.

**opération asynchrone**

Opération qui renvoie le contrôle au programme appelant sans attendre que l'opération se termine. Avant la fin de l'opération, l'exécution du code se poursuit. Voir aussi **opération synchrone**.

Retour au début

## <a name="b"></a>B

**entrée de liaison**

Mappage entre un champ dans une table et une variable. Dans les extensions Visual C++ ADO, les champs de l' **objet Recordset** sont mappés aux variables C/C++.

**composé**

Valeur numérique destinée à une comparaison de valeurs bit par bit avec d'autres valeurs numériques, généralement pour marquer des options dans des valeurs de paramètre ou de retour. En règle générale, cette comparaison est réalisée avec des opérateurs logiques de bits, comme and et **&** **or** dans Visual Basic et **|** dans C++. ****

Par exemple, les valeurs **FIELDATTRIBUTEENUM** ADO peuvent être utilisées en tant que masques de masques pour déterminer les attributs d'un champ. Supposons que vous souhaitiez déterminer si un champ a été mis à jour. Vous pouvez tester ceci à l'aide de l'expression suivante dans Visual Basic:  
  

Si le résultat est TRUE, le champ peut être mis à jour.

**bookmark**

Marqueur qui identifie de manière unique une ligne au sein d'un ensemble de lignes afin qu'un utilisateur puisse y accéder rapidement.

**objet métier**

Objet qui effectue un ensemble défini d'opérations, telles que la validation de données ou la logique de règle métier. Les objets métier résident généralement sur le niveau intermédiaire.

**règle métier**

Combinaison des modifications de validation, des vérifications d'ouverture de session, des recherches dans la base de données, des stratégies et des transformations algorithmiques qui constituent le mode de travail de l'entreprise. Également appelé « *logique métier*».

Retour au début

## <a name="c"></a>C

**expression calculée**

Expression qui n'est pas constante, mais dont la valeur dépend d'autres valeurs. Pour être évaluée, une expression calculée doit obtenir et calculer des valeurs d'autres sources, généralement dans d'autres champs ou lignes.

**ch**

Référence à une plage de lignes d'une source de données. Dans ADO, un chapitre est généralement une référence à un autre **jeu d'enregistrements**.

Les colonnes de chapitre permettent de définir une relation *parent-enfant* dans laquelle le *parent* est l'objet **Recordset** contenant la colonne de chapitre et l'*enfant* est l'objet **Recordset** représenté par le chapitre.

**chapter-alias**

Alias qui fait référence à la colonne ajoutée au parent.

**jeu de caractères**

Mappage d'un jeu de caractères à leurs valeurs numériques. Par exemple, Unicode est un jeu de caractères 16 bits capable de coder tous les caractères connus et utilisé comme norme de codage de caractères dans le monde entier.

**derniers**

Côté dépendant d'une relation hiérarchique. Un enfant est un nœud dans une structure hiérarchique qui a un autre nœud au-dessus de lui (plus proche de la racine). Voir aussi **enfant-alias**, **relation parent-enfant**, **parent**.

**child-alias**

Alias qui fait référence à l'enfant. Voir aussi **alias**, **Child**.

**CLSID (identificateur de classe)**

Identificateur universel unique (UUID) qui identifie un composant COM. Chaque composant COM a son CLSID dans le Registre Windows de sorte qu'il puisse être chargé par d'autres applications. Voir aussi **ProgID**, **com**.

**couche client**

Couche logique d'un système distribué qui présente généralement les données à l'utilisateur et traite les entrées de l'utilisateur, parfois appelé « *frontal*». En règle générale, la couche cliente demande des données à un serveur en fonction de l'entrée, puis met en forme et affiche le résultat. Voir aussi **niveau intermédiaire**, **niveau source de données**, **application distribuée**.

**COM (Component Object Model)**

Norme binaire qui permet aux objets d'interagir dans un environnement en parallèle, indépendamment de la langue dans laquelle ils ont été développés ou sur les ordinateurs sur lesquels ils résident. Les technologies COM incluent les contrôles ActiveX, l'automatisation et la liaison et l'incorporation d'objets (OLE). COM permet à un objet d'exposer ses fonctionnalités à d'autres composants et d'héberger des applications. Il définit la manière dont l'objet s'expose, ainsi que le fonctionnement de cette exposition entre les processus et les réseaux. COM définit également le cycle de vie de l'objet.

**Composant COM**

Fichier binaire, tel que. dll,. ocx et certains fichiers. exe, qui prend en charge la norme COM pour fournir des objets. Ce type de fichier contient le code pour une ou plusieurs références de classe, classes COM, mécanismes d'entrée dans le registre, code de chargement, etc.

**opérateur de comparaison**

Opérateur comparant deux expressions et renvoyant une valeur booléenne.

Paramètre de critère pouvant être exprimé sous la forme\>«» (supérieur à),\<«» (inférieur à), «=» (égal à)\>, «=» (supérieur ou égal à)\<, «=» (inférieur ou égal à)\<\>, «» (différent de) ou «like» (critères spéciaux).

**component**

Objet qui encapsule à la fois les données et le code, et fournit un ensemble bien spécifié de services accessibles au public.

**fichier composé**

Une implémentation du stockage structuré COM pour les fichiers. Un fichier composé stocke des objets distincts dans un seul fichier structuré constitué de deux éléments principaux: les objets de stockage et les objets de flux. Ensemble, ils fonctionnent comme un système de fichiers dans un fichier. Pour plus d'informations, consultez la rubrique fichiers composés dans le kit de développement Microsoft Platform SDK.

Un nombre de fichiers individuels liés dans un même fichier physique. Il est possible d'accéder à chaque fichier dans un fichier composé comme s'il s'agissait d'un fichier physique unique.

**permanente**

Valeur numérique ou de chaîne qui ne change pas. Les énumérations ADO nommées (constantes énumérées) peuvent être utilisées dans votre code au lieu des valeurs réelles, par exemple, **adUseClient** est une constante dont la valeur est 3. (Const adUseClient = 3). Voir aussi **énumération**.

**curseur**

Élément de base de données qui contrôle la navigation dans l'enregistrement, la mise à jour des données et la visibilité des modifications apportées à la base de données par d'autres utilisateurs.

Retour au début

## <a name="d"></a>D

**liaison de données**

Processus d'association des objets ou des contrôles d'une application à une source de données. Un contrôle associé à une source de données est appelé *contrôle lié aux données*.

Le contenu d'un contrôle lié aux données est associé aux valeurs d'une base de données. Par exemple, un contrôle Grid lié à un objet **Recordset** peut être mis à jour lors de la mise à jour des lignes de l'objet **Recordset** . Lorsque de nouvelles valeurs sont récupérées par l' **objet Recordset**, les nouvelles valeurs s'affichent dans la grille.

**fournisseur de données**

Logiciel qui expose des données à une application ADO, directement ou via un fournisseur de services. Voir aussi **fournisseur de services**.

**mise en forme des données**

Technique qui utilise une syntaxe formalisée (appelée **langage de forme**) pour définir un objet Recordset **** spécialisé (appelé un objet **Recordset mis**en forme) qui ne contient pas seulement des données, mais aussi des références à d'autres objets **Recordset** et //valeurs calculées basées sur ces **** autres objets Recordset.

**niveau de la source de données**

Couche logique d'un système distribué qui représente un ordinateur exécutant un SGBD, tel qu'une base de données SQL Server. Voir aussi **niveau client**, **niveau intermédiaire**, **application distribuée**.

**APPELER**

Protocole de transmission qui permet aux composants COM de communiquer directement entre eux sur un réseau. Voir aussi **com**, **composant**.

**DDL (langage de définition de données)**

Instructions en SQL qui définissent, par opposition à manipuler, des données. Le schéma d'une base de données est créé ou modifié avec DDL. Par exemple, **Create table**, **Create index**, **Grant**et **Revoke** sont des instructions SQL DDL.

**flux par défaut**

Un flux de texte ou binaire (représenté par un objet **Stream** ) associé à des objets **Record** ou **Recordset** lors de l'utilisation de certains fournisseurs OLE DB, tels que le fournisseur Microsoft OLE DB pour la publication Internet. Le flux par défaut contient généralement le contenu d'un fichier, tel que le code HTML pour la racine d'un site Web.

**application distribuée**

Programme rédigé de sorte que le traitement puisse être réparti sur plusieurs ordinateurs sur un réseau. En règle générale, une application distribuée est divisée en couches de présentation, de logique métier et de magasin de données, ou de *niveaux*. Voir aussi niveau **client**, niveau **intermédiaire**, **niveau source de données**.

**Recordset déconnecté**

Objet **Recordset** dans un cache client qui n'a plus de connexion active au serveur. Si la source de données d'origine doit être réutilisée pour une raison quelconque, telle que la mise à jour des données, la connexion doit être rétablie. Toutefois, il est toujours possible d'accéder aux collections, propriétés et méthodes d'un **objet Recordset** déconnecté.

**DLL (bibliothèque de liens dynamiques)**

Fichier qui contient une ou plusieurs fonctions qui sont compilées, liées et stockées indépendamment des processus qui les utilisent. Le système d'exploitation mappe les dll dans l'espace d'adressage du processus appelant lors du démarrage du processus ou pendant son exécution.

**DML (langage de manipulation de données)**

Instructions en SQL qui manipulent, par opposition à définir, des données. Les valeurs d'une base de données sont sélectionnées et modifiées avec DML. Par exemple, **Insert**, **Update**, **Delete**et **Select** sont des instructions DML SQL.

**fournisseur de sources de documents**

Classe spéciale de fournisseurs qui gèrent des dossiers et des documents. Lorsqu'un document est représenté par un objet **Record** ou qu'un dossier de documents est représenté par un objet **Recordset** , le fournisseur de sources de documents remplit ces objets d'un ensemble unique de champs qui décrivent les caractéristiques du document. au lieu du document lui-même. Voir aussi **enregistrement de ressource**.

**DSN (nom de source de données)**

Collection d'informations utilisée pour connecter votre application à une base de données ODBC particulière. Le gestionnaire de pilotes ODBC utilise ces informations pour créer une connexion à la base de données. Un DSN peut être stocké dans un fichier (DSN de fichier) ou dans le Registre Windows (un DSN de l'ordinateur).

**Dynamic, propriété**

Propriété propre à un fournisseur de données ou au service de curseur. La collection **Properties** d'un objet est renseignée automatiquement («dynamiquement»). Un objet ne possède pas de propriétés dynamiques tant qu'il n'est pas connecté à une source de données par le biais d'un fournisseur de données particulier. Voir aussi **fournisseur de données**, **curseur**.

Retour au début

## <a name="e-i"></a>E-I

**AnchorStyles**

Liste de constantes nommées. Les valeurs énumérées n'ont pas besoin d'être uniques. Toutefois, le nom de chaque valeur doit être unique dans l'étendue dans laquelle l'énumération est définie. Dans ADO, les énumérations sont utilisées pour les paramètres numériques et les valeurs de retour, pour ajouter une signification au code ADO et pour protéger le développeur des valeurs numériques (qui peuvent changer de la version à la version). Par exemple, pour ouvrir un **jeu d'enregistrements**statique, utilisez la valeur énumérée **adOpenStatic** :  
  

Également appelé *constante énumérée*. Voir aussi **constant**.

**event**

Action reconnue par un objet, pour laquelle vous pouvez écrire du code pour répondre. Les événements peuvent être générés par l'exécution de commandes, la saisie semi-automatique, la navigation dans un jeu d'enregistrements et les mises à jour de données, entre autres actions. Voir aussi **Gestionnaire d'événements**.

**gestionnaire d’événements**

Un gestionnaire d'événements est le code exécuté lorsqu'un événement se produit. Voir aussi **événement**.

**handler**

Routine qui gère une condition ou une opération commune et relativement simple, telle que la récupération d'erreur ou la gestion des données.

**Recordset hiérarchique**

**Objet Recordset** qui contient un autre **jeu d'enregistrements**. Voir aussi mise en **forme des données**, **chapitre**.

Pour plus d'informations, consultez [la rubrique accès aux lignes d'un jeu d'enregistrements hiérarchique](accessing-rows-in-a-hierarchical-recordset.md)

**hiérarchique**

En règle générale, une hiérarchie est une structure classée avec des niveaux supérieurs et subordonnés. Dans ADO, les **jeux d'enregistrements** hiérarchiques sont utilisés pour représenter la relation parent-enfant entre un enregistrement et un chapitre. Par ailleurs, dans ADO, les objets **Record** et **Stream** peuvent être utilisés pour accéder à des structures arborescentes hiérarchiques telles qu'un dossier et des documents. ADO MD inclut également des objets **Hierarchy** pour représenter une relation entre les niveaux d'une dimension dans un cube OLAP. Voir aussi **jeux d'enregistrements hiérarchiques**, **relation parent-enfant**, **Chapter**, **Tree**.

**ISAPI (Internet Server Application Programming Interface)**

Ensemble de fonctions pour les serveurs Internet, tels qu'un serveur Windows NT Server/Windows 2000 exécutant Microsoft Internet Information Services (IIS).

Retour au début

## <a name="k-m"></a>K-M

**key**

Colonne ou colonne d'une table qui identifie de manière unique une ligne; souvent utilisé pour indexer une table.

**marshaling du**

Processus d'empaquetage, d'envoi et de décompression des paramètres de méthode d'interface à travers les limites de thread ou de processus.

**niveau intermédiaire**

Couche logique dans un système distribué entre une interface utilisateur ou un client Web et la base de données. En règle générale, c'est ici que les objets métier sont instanciés. Le niveau intermédiaire est une collection de règles et de fonctions métier qui génèrent et fonctionnent lors de la réception d'informations. Elles effectuent ces opérations par le biais de règles métier, qui peuvent changer fréquemment et sont donc encapsulées dans des composants qui sont physiquement séparés de la logique d'application elle-même. Également appelé *niveau serveur d'applications*. Voir aussi **application distribuée**, **niveau client**, **niveau source de données**.

**MIME (Multi-Purpose Internet Mail extension)**

Protocole Internet développé à l'origine pour permettre l'échange de messages électroniques avec du contenu enrichi sur des environnements réseau, ordinateur et de messagerie hétérogènes. En pratique, MIME a également été adopté et étendu par des applications non-messagerie.

MIME est une norme qui permet la publication et la lecture de données binaires sur Internet. L'en-tête d'un fichier contenant des données binaires contient le type MIME des données; Cela indique aux programmes clients (navigateurs Web et packages de courrier, par exemple) qu'ils doivent gérer les données d'une manière différente de celle de la gestion du texte. Par exemple, l'en-tête d'un document Web contenant un graphique JPEG contient le type MIME propre au format de fichier JPEG. Cela permet à un navigateur d'afficher le fichier avec sa visionneuse JPEG, le cas échéant.

Retour au début

## <a name="n-o"></a>N-O

**UD**

Élément dans une arborescence hiérarchique. Un nœud peut être la racine ou l'enfant d'un autre nœud. Un nœud peut également être le parent de plusieurs enfants. Voir aussi **hiérarchie**, **arborescence**, **racine**, **enfant**, **parent**.

**variable objet**

Variable qui contient une référence à un objet. Par exemple, objCustomObject est une variable qui pointe vers un objet de type CustomObject:  
  
est une variable qui pointe vers un objet de type CustomObject:  
  
Set objCustomObject = CreateObject (ADODB. Recordset

**ODBC (Open Database Connectivity)**

Interface de langage de programmation standard utilisée pour la connexion à diverses sources de données. Il est généralement accessible via le panneau de configuration, où les noms de sources de données (DSN) peuvent être affectés pour utiliser des pilotes ODBC spécifiques.

**OLE DB**

Ensemble d'interfaces qui exposent des données à partir de plusieurs sources à l'aide de COM. Les interfaces OLE DB fournissent aux applications un accès uniforme aux données stockées dans diverses sources d'informations. Ces interfaces prennent en charge la quantité de fonctionnalités SGBD appropriée à la source de données, ce qui lui permet de partager ses données. Voir aussi **com**.

**verrouillage optimiste**

Type de verrouillage dans lequel la page de données contenant un ou plusieurs enregistrements, y compris l'enregistrement en cours de modification, est indisponible pour les autres utilisateurs uniquement lorsque l'enregistrement est mis à jour par la méthode de **mise à** jour, mais disponible avant et après l'appel de la méthode **Update** . .

Le verrouillage optimiste est utilisé lorsque **** l'objet Recordset est ouvert avec le paramètre ou la propriété **LockType** défini sur **adLockOptimistic** ou sur **adLockBatchOptimistic**. Voir aussi **verrouillage pessimiste**.

**valeur ordinale**

Emplacement numérique d'un élément au sein d'une commande. Dans une collection ADO, la valeur ordinale du premier élément est zéro (0). L'élément suivant est un (1), et ainsi de suite.

Retour au début

## <a name="p"></a>P

**commande paramétrée**

Une requête ou une commande qui vous permet de définir des valeurs de paramètre avant l'exécution de la commande. Par exemple, une chaîne SQL peut être paramétrée en incorporant des marqueurs de paramètres dans la chaîne SQL (désignée par le caractère «?»). L'application spécifie ensuite les valeurs de chaque paramètre et exécute la commande.

**transparente**

Côté contrôle d'une relation hiérarchique. Dans une structure hiérarchique, un parent possède un ou plusieurs nœuds enfants situés directement en dessous dans la hiérarchie. Voir aussi **parent-alias**, **parent-enfant Relationship**, **Child**.

**parent-alias**

Alias qui fait référence au parent. Voir aussi **alias**, **parent**.

**relation parent-enfant**

Relation dans une structure hiérarchique dans laquelle le parent se trouve à un niveau plus élevé et directement associé à un ou plusieurs enfants. Un enfant est inférieur d'un niveau et doit avoir un parent. Voir aussi **parent**, **enfant**.

**continue**

Pour enregistrer les données dans un état permanent, par exemple en enregistrant un **objet Recordset** dans un fichier.

**verrouillage pessimiste**

Type de verrouillage dans lequel la page contenant un ou plusieurs enregistrements, y compris l'enregistrement en cours de modification, est indisponible pour les autres utilisateurs afin de s'assurer qu'une mise à jour est effectuée. Le comportement de verrouillage pessimiste est défini par le fournisseur OLE DB. En règle générale, les enregistrements sont verrouillés lors de la modification et ne sont pas disponibles tant que la méthode **Update** n'est pas terminée.

Le verrouillage pessimiste est activé lorsque l' **** objet Recordset est ouvert avec le paramètre ou la propriété **LockType** défini sur **adLockPessimistic**. Voir aussi **verrouillage optimiste**.

**regroupement connexions**

Optimisation des performances basée sur l'utilisation de collections de ressources pré-allouées, telles que des objets ou des connexions de base de données. Il est plus efficace de dessiner une ressource existante à partir du pool que de créer une ressource.

**ProgID (identificateur programmatique)**

Nom unique mappé au registre Windows par une application COM. Le ProgID d'une connexion ADO est «ADODB. Connection ". Voir aussi **CLSID**, **com**.

**proxy**

Objet spécifique à l'interface qui fournit le marshaling et la communication des paramètres requis pour qu'un client appelle un objet application qui s'exécute dans un environnement d'exécution différent, par exemple sur un autre thread ou dans un autre processus. Le proxy est situé avec le client et communique avec un stub correspondant qui est situé avec l'objet application qui est appelé. Voir aussi **stub**.

Retour au début

## <a name="r"></a>R

**URL relative**

URL partiellement qualifiée spécifiant une ressource sur Internet ou un intranet dont l'emplacement est relatif à un point de départ spécifié par une URL absolue ou un objet de connexion ADO équivalent. En effet, les URL absolues et relatives consitute une URL complète. Voir aussi **URL** et **URL absolue**.

**source de données distante**

Source de données qui existe sur un autre ordinateur, plutôt que sur le système local (où l'application cliente s'exécute).

**enregistrement de ressource**

Enregistrement d'un fournisseur de source de documents qui contient des champs pour la définition et la description d'un dossier ou d'un document. Le document lui-même n'est pas contenu dans l'enregistrement de ressource, mais est généralement accessible par le flux par défaut ou par un champ dans l'enregistrement de ressource contenant une URL. Voir aussi **fournisseur de source de document**, **flux par défaut**, **URL**.

**root**

Niveau supérieur dans une arborescence hiérarchique. Le nœud racine n'a pas de parent, mais peut avoir des enfants. Voir aussi **hiérarchie**, **arborescence**, **parent**, **enfant**.

**DSO**

Ensemble de lignes provenant d'une source de données, qui ont toutes le même schéma de champ. Un jeu de lignes peut représenter un ou plusieurs champs d'une table. Un jeu de lignes peut également représenter une table virtuelle, créée par une requête ou une jointure de deux ou plusieurs tables. Dans ADO, les jeux de lignes **** sont représentés par des objets Recordset.

Retour au début

## <a name="s"></a>S

**modèles**

Description d'une base de données pour le système de gestion de base de données (SGBD), généralement générée à l'aide du langage de définition de données fourni par le SGBD. Un schéma définit les attributs de la base de données, tels que les tables, les colonnes et les propriétés.

**étendue**

Plage de référence pour un objet ou une variable ou une plage d'enregistrements dans une vue ou une table. Par exemple, les variables locales peuvent être référencées uniquement dans la procédure dans laquelle elles ont été définies. Les variables publiques sont accessibles à partir de n'importe où dans l'application. Les objets, tels que la base de données active, sont dans l'étendue s'ils se trouvent dans le chemin de recherche défini. Il est possible de spécifier des plages d'enregistrements à l'aide d'une clause Scope dans de nombreuses commandes.

**fournisseur de services**

Logiciel qui encapsule un service en produisant et en consommant des données, ce qui augmente les fonctionnalités de vos applications ADO. Il s'agit d'un fournisseur qui n'expose pas directement les données, mais fournit un service, tel que le traitement des requêtes. Le fournisseur de services peut traiter les données fournies par un fournisseur de données. Voir aussi **fournisseur de données**.

**objet Recordset mis en forme**

**Objet Recordset** dont les colonnes ont été spécifiquement définies pour contenir des données, mais également des références (appelées chapitres) à d'autres objets **Recordset** et/ou des valeurs calculées basées sur d'autres objets **Recordset** .

**sibling**

Deux nœuds ou plus dans une structure hiérarchique qui se trouvent au même niveau dans la hiérarchie. Le nœud racine d'une hiérarchie n'a pas de frères.

**procédure stockée**

Collection de code précompilée, telle que les instructions SQL et les instructions facultatives de contrôle de flux, stockées sous un nom et traitées en tant qu'unité. Les procédures stockées sont stockées dans une base de données; elles peuvent être exécutées avec un appel à partir d'une application et autoriser les variables déclarées par l'utilisateur, l'exécution conditionnelle et d'autres fonctionnalités de programmation puissantes.

**substitution**

Objet spécifique à l'interface qui fournit le marshaling et la communication des paramètres requis pour qu'un objet application reçoive des appels à partir d'un client qui s'exécute dans un autre environnement d'exécution, par exemple sur un autre thread ou dans un autre processus. Le stub se trouve à l'aide de l'objet application et communique avec un proxy correspondant qui est situé avec le client qui l'appelle. Voir aussi **proxy**.

**sous-nœud**

Voir **Child**.

**opération synchrone**

Une opération lancée par du code qui se termine avant que l'opération suivante ne commence. Voir aussi **opération asynchrone**.

Retour au début

## <a name="t-w"></a>T-W

**TreeView**

Structure représentant une relation hiérarchique entre des éléments (nœuds). Il y a un nœud au niveau supérieur d'une arborescence (racine). Sous la racine, il peut y avoir plusieurs enfants. Chaque enfant peut à son tour être le parent d'autres enfants, ce qui revient à un arbre. Un dossier contenant des documents et d'autres dossiers est un exemple type d'arborescence. Voir aussi **hiérarchie**, **nœud**, **racine**, **enfant**, **parent**.

**URL (Uniform Resource Locator)**

Spécifie l'emplacement d'une ressource résidant sur Internet ou sur un intranet. Une URL complète se compose d'un modèle (par exemple, FTP, HTTP, mailto, file, etc.), suivi d'un signe deux-points, d'un nom de serveur et du chemin d'accès complet d'une ressource (par exemple, un document, un graphique ou un autre fichier). Voici quelques exemples d'URL:  
  
- https://www.domain.com/default.html  
- FTP://ftp.Server.Somewhere/FTP.file  
  
- FTP://ftp.Server.Somewhere/FTP.file  
- file://Server/Share/File.doc

Voir aussi **URL absolue** et **URL relative**.

**serveur Web**

Ordinateur qui fournit des services Web et des pages à des utilisateurs intranet et Internet.



