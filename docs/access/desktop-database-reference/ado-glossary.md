---
title: Glossaire ActiveX Data Objects (ADO)
TOCTitle: ADO Glossary
ms:assetid: 40f00876-7525-4117-8f57-f3d87c54be99
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249184(v=office.15)
ms:contentKeyID: 48544438
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9b9fd656aeda727cc829ab47ea4cb9fab8f2a169
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997790"
---
# <a name="ado-glossary"></a>Glossaire ADO

**S’applique à**: Access 2013, Office 2013

## <a name="a"></a>A

**URL absolue**

Une URL complète qui spécifie l’emplacement d’une ressource résidant sur Internet ou un intranet. Voir aussi **URL** et **URL relative**.

**Contrôle ActiveX**

Inscription automatique, dans le processus composant COM qui a souvent un élément visuel au moment du design ou d’exécution. Les contrôles ActiveX ont également la possibilité de communiquer avec un conteneur de documents actifs, tels que Microsoft Internet Explorer.

**ADISAPI (Advanced Data Internet Server Application Programming Interface)**

ISAPI DLL qui fournit l’analyse, le contrôle Automation, le marshaling des **objets Recordset** et la création de packages MIME. Le composant ADISAPI fonctionne par le biais de l’API fournie par Internet Information Services (IIS). Voir aussi **ISAPI**.

**fonction d’agrégation**

Dans une requête, une fonction comme COUNT, AVG ou STDEV qui calcule une valeur à l’aide de toutes les lignes d’une colonne d’une table. Écrire des expressions et dans la programmation, vous pouvez utiliser les fonctions d’agrégation SQL (y compris celles décrites ci-dessus) et des fonctions de regroupement domaine pour déterminer différentes statistiques.

**alias**

Un autre nom que vous donnez à une colonne ou une expression dans une instruction SQL SELECT, souvent plus courte ou plus explicite. Par exemple BobSales correspond à l’alias de l’instruction SELECT suivante : « Select wr-Sales as BobSales from SalesDB ». Un alias peut être utilisé pour assigner dynamiquement des colonnes aux liaisons sur l’objet **DataControl** de contrôle.

**cloisonnement des threads**

Modèle dans lequel tous les appels à un objet se produisent sur un thread de thread COM. Dans cloisonnement sans thread, COM synchronise et marshale les appels. Voir aussi **COM**.

**opération asynchrone**

Une opération qui retourne le contrôle au programme appelant sans attendre que l’opération se termine. Avant que l’opération est terminée, l’exécution du code se poursuit. Voir aussi **opération synchrone**.

Retour au début

## <a name="b"></a>B

**entrée de liaison**

Un mappage entre un champ dans une table et une variable. Dans les extensions ADO Visual C++, les champs du **Recordset** sont mappées à des variables C/C++.

**masque de bits**

Une valeur numérique destiné à une comparaison bit par bit avec les autres valeurs numériques, généralement indiquer les options disponibles dans le paramètre ou les valeurs de retour. Cette comparaison est généralement effectuée avec des opérateurs logiques de bits, telles que **et** et **ou** dans Visual Basic, **&** et **|** en langage C++.

Par exemple, les valeurs de ADO **FieldAttributeEnum** peuvent être utilisées comme masques de bits pour déterminer les attributs d’un champ. Supposons que vous souhaitez déterminer si un champ est modifiable. Pour cela, vous pouvez tester avec l’expression suivante dans Visual Basic :  
  

Si le résultat est TRUE, le champ est modifiable.

**Signet**

Marqueur qui identifie de manière unique une ligne dans un ensemble de lignes afin qu’un utilisateur peut y accéder rapidement.

**objet métier**

Objet qui effectue un ensemble défini d’opérations, telles que logique de règle de validation ou business data. Objets métier résident généralement la couche intermédiaire.

**règle d’entreprise**

La combinaison de validation des modifications, vérifications d’ouverture de session, les recherches de base de données, stratégies et transformations par algorithmes qui constituent le moyen d’une entreprise de votre collaboration. Également connu sous le nom de *la logique métier*.

Retour au début

## <a name="c"></a>C

**expression calculée**

Une expression qui n’est pas une constante, mais dont la valeur dépend d’autres valeurs. Pour être évaluée, une expression calculée doit obtenir et calculer des valeurs à partir d’autres sources, généralement dans les autres champs ou les lignes.

**chapitre**

Une référence à une plage de lignes à partir d’une source de données. Dans ADO, un chapitre est généralement une référence à un autre **jeu d’enregistrements**.

Les colonnes de chapitre permettent de définir une relation *parent-enfant* où le *parent* est l' **objet Recordset** contenant la colonne de chapitre et l' *enfant* est l' **objet Recordset** représenté par le chapitre.

**chapter-alias**

Alias qui fait référence à la colonne ajoutée au parent.

**jeu de caractères**

Un mappage d’un jeu de caractères à leurs valeurs numériques. Par exemple, Unicode est un caractère 16 bits capable de coder tous les caractères connus et son utilisation comme une norme de codage de caractères dans le monde entier.

**enfants**

Le côté dépendant d’une relation hiérarchique. Un enfant est un nœud dans une structure hiérarchique qui possède un autre nœud au-dessus (de plus près à la racine). Voir aussi **alias-enfant**, **relation parent-enfant**, **parent**.

**child-alias**

Alias qui fait référence à l’enfant. Voir aussi **alias**, **enfant**.

**CLSID (identificateur de classe)**

Un identificateur universel unique (UUID) qui identifie un composant COM. Chaque composant COM possède son CLSID dans le Registre Windows afin qu’il peut être chargé par d’autres applications. Voir aussi **ProgID** **COM**.

**couche client**

Couche logique d’un système distribué généralement présente les données aux et traite les entrées de l’utilisateur, parfois appelé le *serveur frontal*. En règle générale, la couche client demande des données à partir d’un serveur basé sur l’entrée, puis mettre en forme et affiche le résultat. Voir aussi **niveau intermédiaire**, **niveau source de données**, **application distribuée**.

**COM (Component Object Model)**

Norme binaire permettant aux objets d’interagir dans un environnement réseau, quelle que soit la langue dans laquelle ils ont été développés ou sur les ordinateurs sur lesquels ils résident. Technologies basées sur COM incluent les contrôles ActiveX, Automation et objets liés et incorporés (OLE). COM permet à un objet d’exposer ses fonctionnalités à d’autres composants et d’héberger des applications. Il définit comment l’objet expose lui-même et comment cette exposition fonctionne sur les processus et les réseaux. COM définit également le cycle de vie de l’objet.

**Composant COM**

Fichiers binaires, telles que .dll, .ocx et certains fichiers .exe, qui prend en charge la norme COM pour fournir des objets. Ce fichier contient le code pour une ou plusieurs références de classe, les classes COM, mécanismes d’entrée dans le Registre, le code de chargement et ainsi de suite.

**opérateur de comparaison**

Un opérateur qui compare deux expressions et renvoie une valeur de type Boolean.

Un paramètre de critères peut être exprimé sous la forme «\>« (supérieur à), »\<« (inférieur à), « = » (égal à), »\>= » (supérieur ou égal à), «\<= » (inférieur ou égal à), «\<\>» (différent de), ou « like » (correspondance).

**component**

Objet qui encapsule des données et le code et fournit un ensemble précis de services disponibles publiquement.

**fichier composé**

Une implémentation de COM structurés de stockage des fichiers. Un fichier composé stocke des objets distincts dans un seul fichier structuré, constitué de deux éléments principaux : objets de stockage et les objets stream. Ensemble, ils fonctionnent comme un système de fichiers dans un fichier. Pour plus d’informations, voir fichiers composés dans le Kit de développement.

Nombre de fichiers liés dans un fichier physique. Chaque fichier dans un fichier composé est accessible comme s’il s’agissait d’un seul fichier physique.

**constante**

Une valeur numérique ou de chaîne qui ne change pas. Énumérations ADO nommées (constantes énumérées) peuvent être utilisées dans votre code au lieu des valeurs réelles, par exemple, **adUseClient** est une constante dont la valeur est 3. (AdUseClient const = 3). Voir aussi **énumération**.

**curseur**

Un élément de base de données qui contrôle la navigation entre les enregistrements, mise à jour des données et la visibilité des modifications apportées à la base de données par d’autres utilisateurs.

Retour au début

## <a name="d"></a>D

**liaison de données**

Le processus d’association d’objets ou contrôles d’une application à une source de données. Un contrôle associé à une source de données est appelé un *contrôle lié aux données*.

Le contenu d’un contrôle lié aux données est associé à des valeurs à partir d’une base de données. Par exemple, un contrôle de grille est lié à un objet **Recordset** peut être mis à jour lors de la mise à jour les lignes dans le **jeu d’enregistrements** . Lorsque de nouvelles valeurs sont récupérées par le **jeu d’enregistrements**, les nouvelles valeurs sont affichés dans la grille.

**fournisseur de données**

Logiciel qui expose des données à une application ADO directement ou via un fournisseur de services. Voir aussi **fournisseur de services**.

**mise en forme des données**

Technique qui utilise une syntaxe formelle (appelée **langue de forme**) pour définir un objet **Recordset** spécialisé (appelé un **objet Recordset mis**) qui contient des données non seulement, mais aussi des références à d’autres objets **Recordset** et et/ou les valeurs en fonction de ces autres objets **Recordset** calculées.

**niveau source de données**

Couche logique d’un système distribué qui représente un ordinateur qui exécute un SGBD, comme une base de données SQL Server. Voir aussi **niveau client**, **niveau intermédiaire**, **application distribuée**.

**DCOM**

Protocole qui permet aux composants COM de communiquer directement entre eux via un réseau. Voir aussi **COM**, **composant**.

**DDL (Data Definition Language)**

Ces instructions SQL qui définissent, par opposition à manipuler les données. Le schéma de base de données est créé ou modifié avec DDL. Par exemple, **CREATE TABLE**, **CREATE INDEX**, **GRANT**et **REVOKE** sont des instructions DDL SQL.

**flux de données par défaut**

Flux textuel ou binaire (représenté par un objet **Stream** ) qui est associé à des objets **Record** ou **Recordset** lors de l’utilisation de certains fournisseurs OLE DB, tel que le fournisseur Microsoft OLE DB pour la publication Internet. Le flux par défaut contient généralement le contenu d’un fichier tel que le code HTML pour la racine d’un site Web.

**application distribuée**

Un programme écrit afin que le traitement peut être réparti sur plusieurs ordinateurs sur un réseau. En règle générale, une application distribuée est divisée en présentation, logique métier et couches de magasin de données ou *des couches*. Voir aussi **niveau client**, **niveau intermédiaire**, **niveau source de données**.

**objet Recordset déconnecté**

Un objet **Recordset** dans un cache client qui ne dispose plus connecté au serveur. Si la source de données d’origine doit être accessible pour une raison quelconque, telles que la mise à jour des données, la connexion doit être rétablie. Toutefois, les collections, les propriétés et les méthodes du **jeu d’enregistrements** déconnecté sont toujours accessible.

**DLL (dynamic-link library)**

Un fichier qui contient une ou plusieurs fonctions compilées, liées et stockées séparément des processus qui les utilisent. Le système d’exploitation mappe les DLL dans l’espace d’adressage du processus appelant lors du démarrage ou en cours d’exécution.

**DML (Data Manipulation Language)**

Ces instructions dans SQL qui manipulent, par opposition à définir, des données. Les valeurs dans une base de données sont sélectionnés et modifiés avec DML. Par exemple, **Insertion**, **mise à jour**, **Supprimer**et **Sélectionnez** sont des instructions DML SQL.

**fournisseur de source de document**

Une classe spéciale de fournisseurs qui gèrent les documents et dossiers. Lorsqu’un document est représenté par un objet **Record** , ou un dossier de documents est représenté par un objet **Recordset** , le fournisseur de source de document remplit ces objets avec un ensemble unique de champs qui décrivent les caractéristiques du document, au lieu du document lui-même. Voir aussi **enregistrement de ressource**.

**DSN (nom de source de données)**

L’ensemble des informations utilisées pour se connecter à votre application à une base de données ODBC particulière. Le Gestionnaire de pilote ODBC utilise ces informations pour créer une connexion à la base de données. Une source de données peut être stockée dans un fichier (fichier DSN) ou dans le Registre Windows (DSN système).

**propriété dynamique**

Une propriété spécifique à un fournisseur de données ou le service de curseur. La collection **Properties** d’un objet est automatiquement renseignée avec ces (« de façon dynamique »). Un objet n’a pas de propriétés dynamiques jusqu'à ce qu’il est connecté à une source de données via un fournisseur de données particulière. Voir aussi **fournisseur de données**, **curseur**.

Retour au début

## <a name="e-i"></a>E-I

**énumération**

Une liste de constantes nommées. Valeurs énumérées ne doivent pas être uniques. Toutefois, le nom de chaque valeur doit être unique dans l’étendue où l’énumération est définie. Dans ADO, énumérations sont utilisées pour le paramètre numérique et valeurs de retour, pour ajouter la signification au code ADO et protègent le développeur à partir des valeurs numériques (qui peut changer d’une version à l’autre). Par exemple, pour ouvrir un **jeu d’enregistrements**de statique, utilisez la valeur **adOpenStatic** énumérées :  
  

Également appelé *constante énumérée*. Voir aussi **constante**.

**event**

Action reconnue par un objet pour lequel vous pouvez écrire du code pour répondre. Événements peuvent être générés par l’exécution de commandes, opération, la navigation de jeu d’enregistrements et mises à jour des données, entre autres. Voir aussi **Gestionnaire d’événements**.

**Gestionnaire d’événements**

Un gestionnaire d’événements est le code qui est exécuté lorsqu’un événement se produit. Voir aussi **l’événement**.

**handler**

Une routine qui gère une opération, telles que la gestion de la récupération ou données erreur ou condition courante et relativement simple.

**jeu d’enregistrements hiérarchique**

Un **jeu d’enregistrements** contenant un autre **jeu d’enregistrements**. Voir aussi **mise en forme des données**, **chapitre**.

Pour plus d’informations, consultez [Accès aux lignes d’un jeu d’enregistrements hiérarchique](accessing-rows-in-a-hierarchical-recordset.md)

**hiérarchie**

En règle générale, une hiérarchie est une structure classée avec un haut niveau et des niveaux subordonnés. Dans ADO, hiérarchiques de **jeux d’enregistrements** sont utilisés pour représenter la relation parent-enfant entre un enregistrement et un chapitre. Également dans ADO, les objets **Record** et **Stream** peuvent servir à accéder à des arborescences hiérarchiques telles que des documents et d’un dossier. ADO MD comprend aussi des objets **Hierarchy** afin de représenter une relation entre les niveaux d’une dimension dans un cube OLAP. Voir aussi **jeux d’enregistrements hiérarchiques**, **relation parent-enfant**, **chapitre**, **arborescence**.

**ISAPI (Internet Server Application Programming Interface)**

Un jeu de fonctions pour les serveurs Internet, par exemple un serveur Windows NT Server/Windows 2000, Microsoft Internet Information Services (IIS) en cours d’exécution.

Retour au début

## <a name="k-m"></a>K-M

**clé**

Une ou plusieurs colonnes dans une table qui identifient de manière unique une ligne ; souvent utilisée pour indexer une table.

**marshaling**

Le processus de conditionnement et envoi par-delà interface des paramètres de méthode au-delà des limites de thread ou un processus.

**niveau intermédiaire**

La couche logique dans un système distribué entre un client web ou d’interface de l’utilisateur et la base de données. Il s’agit généralement où les objets métiers sont instanciés. La couche intermédiaire est une collection de règles métier et des fonctions qui génèrent et à utilisent lors de la réception d’informations. Ils cela par le biais de règles métier, qui peuvent changer fréquemment et sont par conséquent encapsulés dans des composants physiquement distincts de la logique d’application. Également appelé *niveau serveur d’applications*. Voir aussi **application distribuée**, **niveau client**, **niveau source de données**.

**MIME (multi-purpose Internet Mail Extension)**

Protocole Internet développé à l’origine pour permettre l’échange de messages électroniques au contenu enrichi entre les environnements de messagerie, l’ordinateur et réseau hétérogène. En pratique, MIME a été également adopté et étendu par des applications extérieurs à la messagerie.

MIME est une norme qui permet de publier et de lire sur Internet des données binaires. L’en-tête d’un fichier contenant des données binaires contient le type MIME des données ; Cela informe les programmes clients (navigateurs web et programmes de messagerie, par exemple) qu’ils doivent gérer les données d’une autre manière qu’ils gèrent le texte brut. Par exemple, l’en-tête d’un document web incluant un graphisme JPEG contient le type MIME spécifique au format de fichier JPEG. Cela permet à un navigateur afficher le fichier avec sa visionneuse JPEG, s’il est présent.

Retour au début

## <a name="n-o"></a>N-O

**nœud**

Un élément dans une arborescence hiérarchique. Un nœud peut être la racine, ou l’enfant d’un autre nœud. Un nœud peut également être le parent de plusieurs enfants. Voir aussi **hiérarchie**, **arborescence**, **racine**, **enfant**, **parent**.

**variable objet**

Variable qui contient une référence à un objet. Par exemple, objCustomObject est une variable qui pointe vers un objet de type CustomObject :  
  
est une variable qui pointe vers un objet de type CustomObject :  
  
Définir objCustomObject = CreateObject (adodb. Jeu d’enregistrements)

**ODBC (Open Database Connectivity)**

Langue interface de programmation standard utilisée pour se connecter à une variété de sources de données. Cela est généralement accessible via le panneau de configuration, où les noms de source de données (DSN) peuvent être assignées à utiliser les pilotes ODBC spécifiques.

**OLE DB**

Un ensemble d’interfaces qui exposent des données provenant de diverses sources via COM. Interfaces OLE DB fournissent des applications avec un accès homogène aux données stockées dans diverses sources d’informations. Ces interfaces prennent en charge les fonctionnalités SGBD appropriées pour la source de données, ce qui permet de partager ses données. Voir aussi **COM**.

**verrouillage optimiste**

Un type de verrouillage dans lequel la page de données contenant un ou plusieurs enregistrements, notamment l’enregistrement en cours de modification, est indisponible aux autres utilisateurs uniquement pendant que l’enregistrement est mis à jour par la méthode de **mise à jour** , mais reste disponible avant et après l’appel à la **mise à jour** .

Verrouillage optimiste est utilisé lorsque l’objet **Recordset** est ouvert avec le paramètre **LockType** ou d’une propriété définie sur **adLockOptimistic** ou **adLockBatchOptimistic**. Voir aussi **verrouillage pessimiste**.

**valeur ordinale**

Emplacement d’un élément dans un ordre numérique. Dans une collection ADO, la valeur ordinale du premier élément est zéro (0). L’élément suivant est un (1) et ainsi de suite.

Retour au début

## <a name="p"></a>P

**commandes paramétrées**

Une requête ou une commande qui vous permet de définir des valeurs de paramètre avant l’exécution de la commande. Par exemple, une chaîne SQL peut être paramétrée en incorporant des marqueurs de paramètres dans la chaîne SQL (désignés par le « ? » caractères). Ensuite, l’application spécifie les valeurs pour chaque paramètre et exécute la commande.

**parent**

Le contrôle côté d’une relation hiérarchique. Dans une structure hiérarchique, un parent possède un ou plusieurs nœuds enfants directement en dessous de lui dans la hiérarchie. Voir aussi **alias-parent**, **relation parent-enfant**, **enfant**.

**parent-alias**

Alias qui fait référence à l’objet parent. Voir aussi **alias**, **parent**.

**relation parent-enfant**

Une relation dans une structure hiérarchique dans laquelle le parent est un niveau supérieur et directement associé à un ou plusieurs enfants. Un enfant est un niveau inférieur et doit avoir un parent. Voir aussi **parent**, **enfant**.

**conserver**

Pour enregistrer les données dans un état permanent, telles que l’enregistrement d’un **objet Recordset** dans un fichier.

**verrouillage pessimiste**

Type de verrouillage dans lequel la page contenant un ou plusieurs enregistrements, notamment l’enregistrement en cours de modification, est indisponible aux autres utilisateurs afin de garantir qu’une mise à jour. Comportement du verrouillage pessimiste est défini par le fournisseur OLE DB. En règle générale, les enregistrements sont verrouillés lors de la modification et restent inaccessibles jusqu'à ce que la méthode de **mise à jour** est terminée.

Verrouillage pessimiste est activé lors de l’objet **Recordset** est ouvert avec le paramètre **LockType** ou la propriété **adLockPessimistic**. Voir aussi **verrouillage optimiste**.

**le regroupement**

Optimisation des performances en fonction de l’utilisation des collections de ressources alloués préalable, tels que des objets ou des connexions de base de données. Il est plus efficace pour extraire une ressource existante du pool que la création d’une nouvelle ressource.

**ProgID (identificateur programmatique)**

Nom unique mappé dans le Registre Windows à une application COM. Le ProgID pour une connexion ADO est « ADODB. Connexion ». Voir aussi **CLSID**, **COM**.

**proxy**

Un objet spécifique à l’interface qui fournit le marshaling de paramètres et communication requis pour un client appeler un objet application qui s’exécute dans un environnement d’exécution différents, tels que sur un thread différent ou dans un autre processus. Le proxy est installé sur le client et communique avec un stub correspondant qui se trouve à l’objet application qui est appelée. Voir aussi **stub**.

Retour au début

## <a name="r"></a>R

**URL relative**

URL partielle indiquant une ressource sur Internet ou un intranet dont l’emplacement est par rapport à un point de départ spécifié par une URL absolue ou d’un objet Connection ADO équivalent. En effet, la concaténé absolue et relative URL constituer une URL complète. Voir aussi **URL** et **URL absolue**.

**source de données distante**

Une source de données qui existe sur un autre ordinateur, plutôt que sur le système local (où l’application cliente s’exécute).

**enregistrement de ressource**

Un enregistrement d’un fournisseur de source de document qui contient des champs pour la définition et la description d’un dossier ou un document. Le document lui-même ne figure pas dans l’enregistrement de ressource, mais généralement accessible par le flux par défaut ou un champ dans l’enregistrement de ressource contenant une URL. Voir aussi **fournisseur de source de document**, **flux de données par défaut**, **URL**.

**racine**

Le niveau supérieur d’une arborescence hiérarchique. Le nœud racine ne possède aucun parent, mais peut avoir des enfants. Voir aussi **hiérarchie**, **arborescence**, **parent**, **enfant**.

**ensemble de lignes**

Un ensemble de lignes à partir d’une source de données, tous ayant le même schéma de champ. Un ensemble de lignes peut représenter tout ou partie des champs d’une table. Un ensemble de lignes peut également représenter une table virtuelle, créée par une requête ou une jointure de deux ou plusieurs tables. Dans ADO, les ensembles de lignes sont représentés par des objets **Recordset** .

Retour au début

## <a name="s"></a>S

**schéma**

Description d’une base de données pour le système de gestion de base de données (SGBD), générée normalement par le langage de définition de données fourni par le SGBD. Un schéma définit les attributs de la base de données, telles que les tables, les colonnes et les propriétés.

**étendue**

La plage de référence pour un objet ou une variable ou une plage d’enregistrements dans une vue ou une table. Par exemple, les variables locales peuvent être référencées que dans la procédure dans laquelle ils ont été définis. Les variables publiques sont accessibles à partir de n’importe où dans l’application. Objets, tels que la base de données en cours sont dans la portée si elles se trouvent dans le chemin de recherche défini. Plages d’enregistrements peuvent être spécifiées avec une clause Scope dans de nombreuses commandes.

**fournisseur de services**

Logiciel qui encapsule un service en produisant et en utilisant des données pour enrichir les fonctionnalités de vos applications ADO. Il s’agit d’un fournisseur qui n’expose pas directement les données, au lieu de cela, il fournit un service, comme le traitement des requêtes. Le fournisseur de services peut traiter des données fournies par un fournisseur de données. Voir aussi **fournisseur de données**.

**objet Recordset mis en forme**

Un **objet Recordset** dont les colonnes ont été spécifiquement définies pour contenir des données, mais également références (appelées chapitres) à d’autres objets **Recordset** et/ou les autres objets **Recordset** en fonction des valeurs calculées.

**frère**

Les deux ou plusieurs nœuds dans une structure hiérarchique qui sont sur le même niveau de la hiérarchie. Le nœud racine dans une hiérarchie ne possède aucun frère.

**procédure stockée**

Une collection précompilée de code tels que des instructions SQL et les instructions de flux de contrôle facultatives stockées sous un nom et traitées comme une unité. Procédures stockées sont stockées dans une base de données ; ils peuvent être exécutées avec un appel à partir d’une application et autoriser des variables déclarées par l’utilisateur, l’exécution conditionnelle et autres fonctionnalités de programmation puissantes.

**stub**

Un objet spécifique à l’interface qui fournit le marshaling de paramètres et la communication nécessaires pour un objet application recevoir des appels à partir d’un client qui s’exécute dans un environnement d’exécution différents, tels que sur un thread différent ou dans un autre processus. Le stub se trouve avec l’objet application et communique avec un proxy correspondant qui se trouve avec le client qui l’appelle. Voir aussi **proxy**.

**nœud secondaire**

Voir **enfant**.

**opération synchrone**

Une opération lancée par du code terminée avant que l’opération suivante peut démarrer. Voir aussi **opération asynchrone**.

Retour au début

## <a name="t-w"></a>T-W

**arborescence**

Structure représentant une relation hiérarchique entre les éléments (nœuds). Il existe un nœud au niveau supérieur d’une arborescence (racine). En dessous de la racine, il peut y avoir plusieurs enfants. Chaque enfant peut être à son tour le parent d’autres enfants, par conséquent branchement comme une arborescence. Un dossier contenant des documents et des autres dossiers est un exemple typique d’une structure d’arborescence. Voir aussi **hiérarchie**, **nœud**, **racine**, **enfant**, **parent**.

**URL (Uniform Resource Locator)**

Spécifie l’emplacement d’une ressource résidant sur Internet ou un intranet. Une URL complète se compose d’un schéma (tels que FTP, HTTP, mailto, fichiers et ainsi de suite), suivi par un signe deux-points, un nom de serveur et le chemin d’accès complet d’une ressource (comme un document, image ou autre fichier). Quelques exemples d’URL sont les suivants :  
  
- https://www.domain.com/default.html  
- FTP://FTP.Server.somewhere/FTP.file  
  
- FTP://FTP.Server.somewhere/FTP.file  
- file://Server/Share/file.doc

Voir aussi **URL absolue** et **URL relative**.

**serveur Web**

Un ordinateur qui fournit des services web et des pages pour les utilisateurs intranet et Internet.



