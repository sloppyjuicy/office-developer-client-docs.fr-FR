---
title: ActiveX glossaire ADO (Data Objects)
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

URL complète qui spécifie l’emplacement d’une ressource qui réside sur Internet ou un intranet. Voir aussi **l’URL** **et l’URL relative.**

**Contrôle ActiveX**

Composant COM auto-inscrit et in-process qui possède souvent un élément visuel au moment de la conception ou au moment de l’opération. ActiveX contrôles ont également la possibilité de communiquer avec un conteneur de documents actifs, tel que Microsoft Internet Explorer.

**ADISAPI (Advanced Data Internet Server Application Programming Interface)**

Une DLL ISAPI qui fournit l’enquête, le contrôle Automation, le marshaling **des recordset** et l’empaquetage MIME. Le composant ADISAPI fonctionne par le biais de l’API fournie par Internet Information Services (IIS). Voir aussi **ISAPI**.

**fonction d’agrégation**

Dans une requête, fonction telle que COUNT, AVG ou STDEV qui calcule une valeur à l’aide de toutes les lignes d’une colonne d’un tableau. En écrivant des expressions et en programmation, vous pouvez utiliser SQL fonctions d’agrégation (y compris les trois répertoriées ci-dessus) et des fonctions d’agrégation de domaine pour déterminer différentes statistiques.

**alias**

Autre nom que vous donnez à une colonne ou une expression dans une SQL SELECT, souvent plus courte ou plus significative. Par exemple, BobSales est l’alias de l’instruction SELECT suivante : « Select wr-Sales as BobSales from SalesDB ». Un alias peut être utilisé pour affecter dynamiquement des colonnes pour contrôler les liaisons sur **l’objet DataControl.**

**threads de threads d’appart**

Modèle de thread COM dans lequel tous les appels à un objet se produisent sur un thread. Dans les threads de threads de threads, COM synchronise et marshale les appels. Voir aussi **COM**.

**opération asynchrone**

Opération qui renvoie le contrôle au programme appelant sans attendre la fin de l’opération. Avant la fin de l’opération, l’exécution du code se poursuit. Voir aussi **l’opération synchrone**.

Retour au début

## <a name="b"></a>B

**entrée de liaison**

Mappage entre un champ d’une table et une variable. Dans les extensions Visual C++ ADO, les champs **recordset** sont mappés à des variables C/C++.

**masque de bits**

Valeur numérique destinée à une comparaison de valeurs bit par bit avec d’autres valeurs numériques, généralement pour indicateurs des options dans les valeurs de paramètre ou de retour. En règle générale, cette comparaison est effectuée avec des opérateurs logiques au bit, tels que **And** et **Or** dans Visual Basic et **&** en **|** C++.

Par exemple, les valeurs **FieldAttributeEnum** ADO peuvent être utilisées comme masques de bits pour déterminer les attributs d’un champ. Supposons que vous vouliez déterminer si un champ était actualisable. Vous pouvez le tester avec l’expression suivante dans Visual Basic :  
  

Si le résultat est TRUE, le champ peut être mis à jour.

**bookmark**

Marqueur qui identifie de manière unique une ligne dans un ensemble de lignes afin qu’un utilisateur puisse y accéder rapidement.

**objet métier**

Objet qui effectue un ensemble défini d’opérations, telles que la validation des données ou la logique de règle métier. Les objets métier résident généralement sur le niveau intermédiaire.

**règle métier**

Combinaison de modifications de validation, de vérifications d’accès, de recherche de bases de données, de stratégies et de transformations algorithmiques qui constituent la façon dont une entreprise fait des affaires. Également appelé *logique métier*.

Retour au début

## <a name="c"></a>C

**expression calculée**

Expression qui n’est pas constante, mais dont la valeur dépend d’autres valeurs. Pour être évaluée, une expression calculée doit obtenir et calculer des valeurs à partir d’autres sources, généralement dans d’autres champs ou lignes.

**chapter**

Référence à une plage de lignes à partir d’une source de données. Dans ADO, un chapitre est généralement une référence à un autre **recordset**.

Les colonnes de chapitre permettent de définir une relation *parent-enfant* dans laquelle le *parent* est l'objet **Recordset** contenant la colonne de chapitre et l'*enfant* est l'objet **Recordset** représenté par le chapitre.

**chapter-alias**

Alias qui fait référence à la colonne qui a été appendée au parent.

**jeu de caractères**

Mappage d’un ensemble de caractères à leurs valeurs numériques. Par exemple, Unicode est un jeu de caractères 16 bits capable de coder tous les caractères connus et utilisé comme standard de codage de caractères dans le monde entier.

**enfant**

Côté dépendant d’une relation hiérarchique. Un enfant est un nœud dans une structure hiérarchique qui a un autre nœud au-dessus (plus près de la racine). Voir aussi **l’alias enfant**, **la relation parent-enfant**, **le parent**.

**child-alias**

Alias qui fait référence à l’enfant. Voir aussi **alias**, **enfant**.

**CLSID (identificateur de classe)**

Identificateur universel unique (UUID) qui identifie un composant COM. Chaque composant COM possède son CLSID dans le Registre Windows afin qu’il puisse être chargé par d’autres applications. Voir aussi **ProgID**, **COM**.

**niveau client**

Couche logique d’un système distribué qui présente et traite généralement les données entrées par l’utilisateur, parfois appelée « *frontal ».* En règle générale, la couche client demande des données à partir d’un serveur en fonction de l’entrée, puis formate et affiche le résultat. Voir aussi **niveau intermédiaire**, niveau source **de données**, application **distribuée**.

**COM (Component Object Model)**

Une norme binaire qui permet aux objets d’interopérer dans un environnement réseau, quelle que soit la langue dans laquelle ils ont été développés ou sur quels ordinateurs ils résident. Les technologies COM incluent les contrôles ActiveX, l’automatisation et la liaison et l’incorporation d’objets (OLE). COM permet à un objet d’exposer ses fonctionnalités à d’autres composants et d’héberger des applications. Il définit à la fois la façon dont l’objet s’expose lui-même et le fonctionnement de cette exposition sur les processus et sur les réseaux. COM définit également le cycle de vie de l’objet.

**Composant COM**

Fichier binaire, tel que .dll, .ocx et certains fichiers .exe, qui prend en charge la norme COM pour la fourniture d’objets. Un tel fichier contient du code pour une ou plusieurs fabriques de classes, classes COM, mécanismes d’entrée de Registre, chargement de code, etc.

**opérateur de comparaison**

Opérateur qui compare deux expressions et renvoie une valeur boolé américaine.

Paramètre de critère qui peut être exprimé sous la forme « ( supérieur à \> ), » (inférieur à), « = » (égal à), « = » (supérieur ou égal à), « = » (inférieur ou égal à), « ( non égal à) » (non égal à) ou « like » \< \> \< \< \> (correspondance de modèle).

**component**

Objet qui encapsule à la fois les données et le code, et fournit un ensemble bien spécifié de services disponibles publiquement.

**fichier composé**

Implémentation du stockage structuré COM pour les fichiers. Un fichier composé stocke des objets distincts dans un fichier structuré unique composé de deux éléments principaux : les objets de stockage et les objets de flux. Ensemble, ils fonctionnent comme un système de fichiers au sein d’un fichier. Pour plus d’informations, voir Fichiers composés dans le SDK de plateforme Microsoft.

Un certain nombre de fichiers individuels liés dans un fichier physique. Chaque fichier d’un fichier composé est accessible comme s’il s’agit d’un seul fichier physique.

**constante**

Valeur numérique ou chaîne qui ne change pas. Les éumérations ADO nommées (constantes éumées) peuvent être utilisées dans votre code au lieu de valeurs réelles, par exemple, **adUseClient** est une constante dont la valeur est 3. (Const adUseClient = 3). Voir aussi **l’éumération**.

**curseur**

Élément de base de données qui contrôle la navigation d’enregistrement, la mise à jour des données et la visibilité des modifications apportées à la base de données par d’autres utilisateurs.

Retour au début

## <a name="d"></a>D

**liaison de données**

Processus d’association des objets ou contrôles d’une application à une source de données. Un contrôle associé à une source de données est appelé contrôle *lié aux données.*

Le contenu d’un contrôle lié aux données est associé aux valeurs d’une base de données. Par exemple, un contrôle de grille lié à un objet **Recordset** peut être mis à jour lorsque les lignes du jeu d’enregistrements **sont** mises à jour. Lorsque de nouvelles valeurs sont récupérées par le **jeu d’enregistrements,** de nouvelles valeurs sont affichées dans la grille.

**fournisseur de données**

Logiciel qui expose les données à une application ADO directement ou via un fournisseur de services. Voir aussi **le fournisseur de services.**

**mise en forme des données**

Technique qui utilise une syntaxe formalisée (appelée Langage de **forme)** pour définir un objet **Recordset** spécialisé (appelé jeu d’enregistrements en **forme)** qui contient non seulement des données, mais également des références à d’autres objets **Recordset** et/ou des valeurs calculées en fonction de ces autres objets **Recordset.**

**niveau de source de données**

Couche logique d’un système distribué qui représente un ordinateur exécutant un SGBD, tel qu’une base SQL Server données. Voir aussi **niveau client**, **niveau intermédiaire**, application **distribuée**.

**DCOM**

Protocole de câblage qui permet aux composants COM de communiquer directement les uns avec les autres sur un réseau. Voir aussi **COM**, **composant**.

**DDL (Data Definition Language)**

Ces instructions dans SQL qui définissent, par opposition à manipuler, les données. Le schéma d’une base de données est créé ou modifié avec DDL. Par exemple, **CREATE TABLE**, **CREATE INDEX,** **GRANT** et **REVOKE** sont SQL instructions DDL.

**flux par défaut**

Texte ou flux binaire (représenté par un objet **Stream)** associé à des objets **Record** ou **Recordset** lors de l’utilisation de certains fournisseurs OLE DB, tels que le fournisseur Microsoft OLE DB pour la publication Internet. Le flux par défaut contient généralement le contenu d’un fichier tel que le code HTML de la racine d’un site web.

**application distribuée**

Programme écrit pour que le traitement puisse être réparti sur plusieurs ordinateurs sur un réseau. En règle générale, une application distribuée est divisée en couches de présentation, de logique métier et de magasin de *données.* Voir aussi **niveau client**, **niveau intermédiaire**, niveau source **de données**.

**recordset déconnecté**

Objet **Recordset** dans un cache client qui ne dispose plus d’une connexion en direct au serveur. Si la source de données d’origine doit être à nouveau accessible pour une raison quelconque, telle que la mise à jour des données, la connexion doit être rétablie. Toutefois, les collections, propriétés et méthodes d’un **recordset** déconnecté sont toujours accessibles.

**DLL (bibliothèque de liens dynamiques)**

Fichier qui contient une ou plusieurs fonctions compilées, liées et stockées séparément des processus qui les utilisent. Le système d’exploitation place les DLLs dans l’espace d’adressale du processus appelant au démarrage du processus ou pendant son exécution.

**DML (langage de manipulation de données)**

Ces instructions dans SQL qui manipulent, au lieu de définir, des données. Les valeurs d’une base de données sont sélectionnées et modifiées avec DML. Par exemple, **INSERT,** **UPDATE,** **DELETE** et **SELECT** sont SQL instructions DML.

**fournisseur de source de documents**

Classe spéciale de fournisseurs qui gèrent les dossiers et les documents. Lorsqu’un document est représenté par un objet **Record** ou qu’un dossier de documents est représenté par un objet **Recordset,** le fournisseur de sources de documents remplit ces objets avec un ensemble unique de champs qui décrivent les caractéristiques du document, au lieu du document lui-même. Voir aussi **l’enregistrement de ressource.**

**DSN (nom de la source de données)**

Collection d’informations utilisées pour connecter votre application à une base de données ODBC particulière. Le gestionnaire de pilotes ODBC utilise ces informations pour créer une connexion à la base de données. Un DSN peut être stocké dans un fichier (un DSN de fichier) ou dans le Registre Windows (un DSN d’ordinateur).

**propriété dynamique**

Propriété spécifique à un fournisseur de données ou au service de curseur. La collection **Properties** d’un objet est remplie automatiquement avec ces éléments ( « dynamiquement »). Un objet n’a aucune propriété dynamique tant qu’il n’est pas connecté à une source de données via un fournisseur de données particulier. Voir aussi **le fournisseur de données,** **le curseur**.

Retour au début

## <a name="e-i"></a>E-I

**enumeration**

Liste des constantes nommées. Les valeurs éumées ne doivent pas être uniques. Toutefois, le nom de chaque valeur doit être unique dans l’étendue dans laquelle l’éumération est définie. Dans ADO, les éumérations sont utilisées pour les valeurs de paramètre numérique et de retour, pour ajouter une signification au code ADO et protéger le développeur des valeurs numériques (qui peuvent changer de version en version). Par exemple, pour ouvrir un **recordset** statique, utilisez la valeur éumée **adOpenStatic** :  
  

Également appelée constante *éumée*. Voir aussi **constante**.

**event**

Action reconnue par un objet, pour laquelle vous pouvez écrire du code pour répondre. Les événements peuvent être générés par l’exécution de la commande, l’achèvement des transactions, la navigation dans le recordset et les mises à jour de données, entre autres actions. Voir aussi **le handler d’événements.**

**gestionnaire d’événements**

Un handler d’événement est le code qui est exécuté lorsqu’un événement se produit. Voir aussi **l’événement**.

**handler**

Routine qui gère une condition ou une opération courante et relativement simple, telle que la récupération d’erreurs ou la gestion des données.

**recordset hiérarchique**

Un **recordset** qui contient un autre **recordset**. Voir aussi **mise en forme des** données , **chapitre**.

Pour plus d’informations, [voir Accessing Rows in a Hierarchical Recordset](accessing-rows-in-a-hierarchical-recordset.md)

**hiérarchie**

En règle générale, une hiérarchie est une structure classée avec un niveau supérieur et des niveaux subordonnés. Dans ADO,  les jeux d’enregistrements hiérarchiques sont utilisés pour représenter la relation parent-enfant entre un enregistrement et un chapitre. En outre, dans ADO, les objets **Record** et **Stream** peuvent être utilisés pour accéder aux structures d’arborescence hiérarchiques telles qu’un dossier et des documents. ADO MD inclut également **des objets Hierarchy** pour représenter une relation entre les niveaux d’une dimension dans un cube OLAP. Voir aussi **jeux d’enregistrements hiérarchiques**, **relation parent-enfant**, **chapitre**, **arborescence**.

**ISAPI (Internet Server Application Programming Interface)**

Ensemble de fonctions pour les serveurs Internet, telles qu’un serveur Windows NT Server/Windows 2000 exécutant Microsoft Internet Information Services (IIS).

Retour au début

## <a name="k-m"></a>K-M

**key**

Une ou plusieurs colonnes dans un tableau qui identifient une ligne de manière unique ; souvent utilisé pour indexer une table.

**marshaling**

Processus d’empaquetage, d’envoi et de décompressage des paramètres de méthode d’interface au-delà des limites de thread ou de processus.

**niveau intermédiaire**

Couche logique dans un système distribué entre une interface utilisateur ou un client web et la base de données. C’est généralement là que les objets métier sont ins instantiés. Le niveau intermédiaire est un ensemble de règles et de fonctions métiers qui génèrent et opèrent sur la réception d’informations. Ils y parviennent par le biais de règles métiers, qui peuvent changer fréquemment et sont donc encapsulées dans des composants physiquement séparés de la logique de l’application elle-même. Également appelé niveau *serveur d’applications.* Voir aussi **application distribuée**, **niveau client**, niveau source **de données**.

**MIME (Extension de messagerie Internet à usage multiple)**

Protocole Internet développé à l’origine pour permettre l’échange de messages électroniques avec du contenu enrichi dans des environnements de réseau, d’ordinateur et de messagerie hétérogènes. Dans la pratique, MIME a également été adopté et étendu par des applications non-courrier.

MIME est une norme qui permet la publication et la lecture de données binaires sur Internet. L’en-tête d’un fichier contenant des données binaires contient le type MIME des données ; Cela informe les programmes clients (navigateurs web et packages de messagerie, par exemple) qu’ils devront gérer les données d’une manière différente de celle de texte direct. Par exemple, l’en-tête d’un document web contenant un graphique JPEG contient le type MIME spécifique au format de fichier JPEG. Cela permet à un navigateur d’afficher le fichier avec sa visionneuse JPEG, s’il en existe une.

Retour au début

## <a name="n-o"></a>N-O

**nœud**

Élément d’une structure d’arborescence hiérarchique. Un nœud peut être la racine ou l’enfant d’un autre nœud. Un nœud peut également être le parent de plusieurs enfants. Voir aussi hiérarchie ,  **arborescence**, racine , **enfant**, **parent**. 

**variable objet**

Variable qui contient une référence à un objet. Par exemple, objCustomObject est une variable qui pointe vers un objet de type CustomObject :  
  
est une variable qui pointe vers un objet de type CustomObject :  
  
Set objCustomObject = CreateObject(adodb. Recordset)

**ODBC (Open Database Connectivity)**

Interface de langage de programmation standard utilisée pour se connecter à diverses sources de données. Cela est généralement accessible via le Panneau de contrôle, où les noms de source de données (DSN) peuvent être affectés pour utiliser des pilotes ODBC spécifiques.

**OLE DB**

Ensemble d’interfaces qui exposent des données provenant de diverses sources à l’aide de COM. Les interfaces OLE DB fournissent aux applications un accès uniforme aux données stockées dans diverses sources d’informations. Ces interfaces permettent de prendre en charge la quantité de fonctionnalités SGBD appropriées à la source de données, ce qui lui permet de partager ses données. Voir aussi **COM**.

**verrouillage optimiste**

Type de verrouillage dans lequel la page de données contenant un ou plusieurs enregistrements, y compris l’enregistrement en cours de modification, n’est disponible pour les autres utilisateurs que pendant que l’enregistrement est mis à jour par la méthode **Update,** mais est disponible avant et après l’appel de **Mise** à jour .

Le verrouillage optimiste est utilisé lorsque l’objet **Recordset** est ouvert avec le paramètre **LockType** ou la propriété **adLockOptimistic** ou **adLockBatchOptimistic**. Voir aussi **verrouillage pessimiste**.

**valeur ordinale**

Emplacement numérique d’un élément dans une commande. Dans une collection ADO, la valeur ordinale du premier élément est zéro (0). L’élément suivant est un (1), et ainsi de suite.

Retour au début

## <a name="p"></a>P

**commande paramétrisée**

Requête ou commande qui vous permet de définir des valeurs de paramètre avant l’exécution de la commande. Par exemple, une chaîne SQL peut être paramétrisée en insérez des marqueurs de paramètres dans la chaîne SQL (désignée par le caractère « ? »). L’application spécifie ensuite des valeurs pour chaque paramètre et exécute la commande.

**parent**

Côté contrôle d’une relation hiérarchique. Dans une structure hiérarchique, un parent a un ou plusieurs nodes enfants directement en dessous dans la hiérarchie. Voir aussi **parent-alias**, **relation parent-enfant**, **enfant**.

**parent-alias**

Alias qui fait référence au parent. Voir aussi **alias**, **parent**.

**relation parent-enfant**

Relation dans une structure hiérarchique dans laquelle le parent est un niveau supérieur et directement associé à un ou plusieurs enfants. Un enfant est d’un niveau inférieur et doit avoir un parent. Voir aussi **parent**, **enfant**.

**persist**

Pour enregistrer des données dans un état permanent, comme l’enregistrement d’un **recordset** dans un fichier.

**verrouillage pessimiste**

Type de verrouillage dans lequel la page contenant un ou plusieurs enregistrements, y compris l’enregistrement en cours de modification, n’est pas disponible pour les autres utilisateurs afin de garantir qu’une mise à jour sera réalisée. Le comportement de verrouillage pessimiste est défini par le fournisseur OLE DB. En règle générale, les enregistrements sont verrouillés lors de la modification et restent indisponibles jusqu’à ce que la méthode **Update** soit terminée.

Le verrouillage pessimiste est activé lorsque l’objet **Recordset** est ouvert avec le paramètre **LockType** ou la propriété **adLockPessimistic**. Voir aussi **verrouillage optimiste**.

**pooling**

Optimisation des performances basée sur l’utilisation de collections de ressources pré-allouées, telles que des objets ou des connexions de base de données. Il est plus efficace de dessiner une ressource existante à partir du pool que de créer une nouvelle ressource.

**ProgID (identificateur programmatique)**

Nom unique mappé au Registre Windows par une application COM. Le ProgID d’une connexion ADO est « ADODB. Connection « . Voir aussi **CLSID**, **COM**.

**proxy**

Objet spécifique à l’interface qui fournit le marshaling de paramètres et la communication requis pour qu’un client appelle un objet d’application qui s’exécute dans un autre environnement d’exécution, par exemple sur un thread différent ou dans un autre processus. Le proxy se trouve avec le client et communique avec un stub correspondant qui se trouve avec l’objet d’application qui est appelé. Voir aussi **stub**.

Retour au début

## <a name="r"></a>R

**URL relative**

URL partiellement qualifiée qui spécifie une ressource sur Internet ou un intranet dont l’emplacement est relatif à un point de départ spécifié par une URL absolue ou un objet de connexion ADO équivalent. En effet, les URL absolues et relatives concatés consituent une URL complète. Voir aussi **URL et** **URL absolue.**

**source de données distante**

Source de données qui existe sur un autre ordinateur, plutôt que sur le système local (où l’application cliente s’exécute).

**enregistrement de ressource**

Enregistrement d’un fournisseur de source de documents qui contient des champs pour la définition et la description d’un dossier ou d’un document. Le document lui-même n’est pas contenu dans l’enregistrement de ressource, mais il est généralement accessible par le flux par défaut ou un champ dans l’enregistrement de ressource contenant une URL. Voir aussi **le fournisseur source de document**, flux par **défaut**, **URL**.

**racine**

Niveau supérieur dans une structure d’arborescence hiérarchique. Le nœud racine n’a pas de parents, mais peut avoir des enfants. Voir aussi **hiérarchie**, **arborescence**, **parent**, **enfant**.

**rowset**

Ensemble de lignes d’une source de données, ayant toutes le même schéma de champ. Un ensemble de lignes peut représenter tout ou partie des champs d’une table. Un ensemble de lignes peut également représenter une table virtuelle, créée par une requête ou une jointrie de deux tables ou plus. Dans ADO, les jeux de lignes sont représentés par des **objets Recordset.**

Retour au début

## <a name="s"></a>S

**schéma**

Description d’une base de données vers le système de gestion de base de données (SGBD), généralement générée à l’aide du langage de définition de données fourni par le SGBD. Un schéma définit les attributs de la base de données, tels que les tables, les colonnes et les propriétés.

**scope**

Plage de références pour un objet ou une variable ou une plage d’enregistrements dans une vue ou une table. Par exemple, les variables locales ne peuvent être référencés que dans la procédure dans laquelle elles ont été définies. Les variables publiques sont accessibles n’importe où dans l’application. Les objets, tels que la base de données actuelle, sont dans l’étendue s’ils sont dans le chemin de recherche défini. Les plages d’enregistrement peuvent être spécifiées avec une clause Scope dans de nombreuses commandes.

**fournisseur de services**

Logiciel qui encapsule un service en produisant et en consommant des données, augmentant ainsi les fonctionnalités de vos applications ADO. Il s’agit d’un fournisseur qui n’expose pas directement les données, mais qui fournit un service, tel que le traitement des requêtes. Le fournisseur de services peut traiter les données fournies par un fournisseur de données. Voir aussi **le fournisseur de données.**

**recordset en forme**

Un **recordset** dont les colonnes ont été spécifiquement définies pour contenir non seulement des données, mais aussi des références (appelées chapitres) à d’autres objets **Recordset** et/ou des valeurs calculées basées sur d’autres objets **Recordset.**

**frère**

Au moins deux nodes dans une structure hiérarchique qui se sont au même niveau dans la hiérarchie. Le nœud racine d’une hiérarchie n’a pas de frères.

**procédure stockée**

Collection précompilée de code telle que des instructions SQL et des instructions de contrôle de flux facultatives stockées sous un nom et traitées en tant qu’unité. Les procédures stockées sont stockées dans une base de données ; Elles peuvent être exécutées avec un seul appel à partir d’une application et autoriser les variables déclarées par l’utilisateur, l’exécution conditionnelle et d’autres fonctionnalités de programmation puissantes.

**stub**

Objet spécifique à l’interface qui fournit le marshaling de paramètres et la communication requis pour qu’un objet d’application reçoie des appels d’un client qui s’exécute dans un autre environnement d’exécution, par exemple sur un thread différent ou dans un autre processus. Le stub se trouve avec l’objet application et communique avec un proxy correspondant qui se trouve avec le client qui l’appelle. Voir aussi **proxy**.

**sous-nœud**

Voir **enfant**.

**opération synchrone**

Une opération initiée par du code qui se termine avant le début de l’opération suivante. Voir aussi **l’opération asynchrone**.

Retour au début

## <a name="t-w"></a>T-W

**tree**

Structure représentant une relation hiérarchique entre les éléments (nodes). Il existe un nœud au niveau supérieur d’une arborescence (racine). Sous la racine, il peut y avoir plusieurs enfants. Chaque enfant peut à son tour être le parent d’autres enfants, ce qui se branche comme une arborescence. Un dossier contenant des documents et d’autres dossiers est un exemple classique d’arborescence. Voir aussi **hiérarchie**, **nœud**, **racine**, **enfant**, **parent**.

**URL (Uniform Resource Locator)**

Spécifie l’emplacement d’une ressource résidant sur Internet ou un intranet. Une URL complète se compose d’un schéma (par exemple, FTP, HTTP, mailto, fichier, et ainsi de suite), suivi d’un deux-points, d’un nom de serveur et du chemin d’accès complet d’une ressource (par exemple, un document, un graphique ou un autre fichier). Voici quelques exemples d’URL :  
  
- https://www.domain.com/default.html  
- ftp://ftp.server.somewhere/ftp.file  
  
- ftp://ftp.server.somewhere/ftp.file  
- file://Server/Share/File.doc

Voir aussi **l’URL absolue** et **l’URL relative.**

**serveur web**

Ordinateur qui fournit des services web et des pages aux utilisateurs intranet et Internet.



