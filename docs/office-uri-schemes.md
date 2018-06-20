---
title: Modèles d’URI Office
manager: luken
ms.date: 01/14/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1ea99a8f-b005-4b92-b313-923294d20fbf
ms.openlocfilehash: 834c4d2c2f47c6cc3f35423a7dfe3c13caf3d209
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782523"
---
# <a name="office-uri-schemes"></a>Modèles d’URI Office

## <a name="11-abstract"></a>1.1 ABSTRACT

Ce document définit le format d’Uniform Resource Identifier (URI) pour les applications de productivité office. Le schéma est pris en charge dans Microsoft Office 2010 Service Pack 2 et versions ultérieures, y compris Microsoft Office 2013 pour Windows et les produits Microsoft SharePoint 2013. Il est également pris en charge dans Office pour iPhone, Office pour iPad et Office pour Mac 2011.
  
## <a name="12-introduction"></a>1.2 PRÉSENTATION DE

Ces modèles URI autoriser pour les applications de productivité office à appeler avec différentes commandes. Chaque application reçoit une autre nommée jeu mais tous les jeux de suivent les mêmes règles pour la façon dont l’URI est formé (schéma URI).
  
## <a name="13-uri-schema"></a>1.3 SCHÉMA D’URI

### <a name="full-schema"></a>Modèle complet

< *nom du schéma* > : < *nom de la commande* > « | » < *descripteur de l’argument commande* > « | » < *argument de commande*  > 
  
Un URI tel que défini dans ce document peut avoir un ou plusieurs arguments de commande, chacun d'entre eux doit inclure < *descripteur de l’argument commande* > et les éléments < *argument de commande* > et être séparé par une barre verticale (« | ») caractères. Lorsque plusieurs arguments de commande est inclus dans un URI il doit y avoir une barre verticale (« | ») caractère en séparant chaque argument de commande de l’argument de commande suivant. 
  
Ces modèles n’incluent pas d’un composant d’autorité telle que définie dans la section 3.2 de RFC 3986. Appel des commandes spécifiée dans ce document s’effectue dans le contexte du système d’appel de la commande. Par exemple, lorsque l’URI « ms-excel : complément | u | http://contoso/Q4/budget.xls« est appelée à partir d’un ordinateur exécutant Microsoft Windows en mode lecture seule de Microsoft Office 2013 installed les attendue résultat est qui les local installation of Microsoft Excel sera Cap lancée et réussite arguments à ouvrir le fichier at *http://contoso/Q4/budget.xls* dans . Notez que la barre verticale est utilisée comme séparateur dans cette spécification n’est pas entre ces caractères identifiés dans la section 2.2 de RFC 3986 comme réservée à un usage potentiels comme séparateurs. Cette opération est effectuée intentionnellement afin d’optimiser le jeu de caractères, l’URI argument de commande peut prendre en charge sans avoir à coder pour cent ces caractères. 
  
La syntaxe du modèle est la suivante :
  
1. < *nom du schéma* > : il s’agit du type d’application qui doit être appelée. Par exemple, le mot ms : nom de jeu de couleurs est enregistré par Microsoft Word. 
    
2. « : » séparateur
    
3. < *nom de la commande* > : cela décrit les actions que l’application doit effectuer. Par exemple, l’ouverture d’un document pour l’afficher. La liste des noms de commande est décrit dans la section 1.5. 
    
4. "|" séparateur (barre verticale)
    
5. < *descripteur de l’argument commande* > : plus d’informations sur l’argument de la commande est sur ce permet d’élément. 
    
6. "|" séparateur (barre verticale)
    
7. < *argument de commande* > : les arguments varient en fonction de la commande. Argument commun est l’URI à un document, généralement à l’aide du schéma http ou https. Notez que dans < *argument de commande* > segments la RFC 3986 réservés caractères « : » et « / » font partie des données argument, pas les délimiteurs et sont par conséquent inclus sans séquence d’échappement. 
    
### <a name="abbreviated-schema"></a>Modèle abrégé

Une forme abrégée des modèles office URI permet à une demande plus compacte pour lancer une application Office spécifiée pour ouvrir la ressource située à un URI donné. Cette forme abrégée implique le complément « < *nom de la commande* > » et le < *descripteur de l’argument commande* > « u ». Aucune des commandes supplémentaires ou des arguments de commande ne sont autorisés dans ce schéma. 
  
< *nom du schéma* > : < *argument de commande*  > 
  
1. < *nom du schéma* > : le type d’application qui doit être appelée. Par exemple ms-word : pour que Microsoft Word. 
    
2. < *argument de commande* > : URI de la ressource, l’application doit s’ouvrir. Actuellement URI uniquement basé sur le protocole http ou https jeu sont prises en charge. 
    
## <a name="14-scheme-names-and-office-application-registrations"></a>1.4 RÉGIME DE NOMS ET LES ENREGISTREMENTS DES APPLICATIONS OFFICE

Voici la liste des noms de schéma utilisés dans des applications Microsoft Office. Lorsque Microsoft Office est installé, chaque nom de jeu de couleurs est enregistré avec Windows sont gérés par le produit Office du même nom. Notez que « ms-spd » est l’abréviation de SharePoint Designer.
  
> - *MS-word :* 
    
> - *MS-powerpoint :* 
    
> - *Microsoft excel :* 
    
> - *MS-visio :* 
    
> - *MS-access :* 
    
> - *MS-projet :* 
    
> - *MS-publisher :* 
    
> - *MS-spd :* 
    
> - *MS-infopath :* 
    
## <a name="15-commands-and-required-command-arguments"></a>1,5 COMMANDES ET DES ARGUMENTS DE LA COMMANDE REQUIS

### <a name="view-document"></a>Afficher un document

La commande suivante entraîne l’ouverture par l’application du document référencé par l’URI en mode lecture seule ou en mode affichage.
  
> Nom de la commande : le complément
    
> Descripteur d’argument de la commande : u
    
> Argument de la commande : URI vers le document, basé sur le schéma http ou https
    
> Exemple : *ms-excel : complément | u |http://contoso/Q4/budget.xls * 
    
### <a name="edit-document"></a>Modifier le Document

La commande suivante provoque l’application ouvrir le document référencé par l’URI en mode édition.
  
> Nom de la commande : dese
    
> Descripteur d’argument de la commande : u
    
> Argument de la commande : URI vers le document, basé sur le schéma http ou https
    
> Exemple : *ms-powerpoint : dese | u |http://www.fourthcoffee.com/AllHandsDeck.ppt * 
    
### <a name="new-document-from-template"></a>Nouveau Document modèle

La commande suivante provoque l’application créer et ouvrir un nouveau document basé sur le modèle stocké à l’URI spécifié. Le fichier de modèle n’est pas modifié dans ce processus. Un argument de commande supplémentaires peut-être être fourni pour spécifier le chemin d’accès par défaut est proposé en tant qu’un enregistrement emplacement lorsque le fichier est le premier enregistrée. Il est possible de l’utilisateur à choisir un emplacement différent.
  
> Nom de commande : nft
    
> Commande descripteur argument 1 : u
    
> L’argument 1 de la commande : un URI dans le modèle, basé sur le schéma http ou https
    
> Descripteur d’argument facultatif commande 2 : s
    
> Argument de commande facultatif 2 : URI spécifiant le dossier d’enregistrement par défaut
    
> Exemple : *ms-word : nft | u |http://cohowinery/templates/elegance.pot| s | http://cohowinery/presentations* 
    
En tant qu’une note, si la valeur par défaut facultative enregistrer emplacement est indiqué, il doit pointer vers le même nom d’hôte en tant que modèle.
  
En outre, les applications SharePoint Designer et InfoPath (qui implémentent la ms-spd : schéma et ms-infopath : régimes, respectivement) ne prennent pas en charge le « nouveau document modèle » fonctionnalité.
  
## <a name="16-backwards-compatibility"></a>1.6 DESCENDANTE COMPATIBILITÉ

Lors de l’analyse un URI pour extraire les arguments de la commande appropriée pour une commande donnée, le Gestionnaire d’URI Office n’utilise les arguments de commande dont le descripteur d’argument de commande attendue. S’il existe des paires d’arguments et des descripteurs de l’argument ayant descripteurs argument inattendu, ils seront supprimés de l’URI. Ce mécanisme permet de futures versions du schéma pour ajouter des arguments de commande supplémentaires sans rompre la compatibilité descendante avec des mises en œuvre de ce schéma.
  
## <a name="17-implementation-restrictions-on-command-arguments"></a>1.7 RESTRICTIONS DE MISE EN ŒUVRE SUR LES ARGUMENTS DE LA COMMANDE

Les restrictions ci-dessous sont appliquées aux arguments de commande dans l’implémentation actuelle dans Office 2013.
  
### <a name="length-limitations-on-uri-command-arguments"></a>Limites de longueur des arguments de la commande URI

Arguments de commande URI, la longueur maximale est de 256 caractères pour toutes les applications à l’exception d’Excel, où la limite est de 216. Les longueurs de chemin d’accès supérieures à ces peuvent être pris en charge sur une base application-par-app et test est recommandé avant de déployer des solutions qui s’appuient sur ce.
  
### <a name="allowed-characters-in-uri-command-arguments"></a>Caractères autorisés dans les arguments de commande d’URI

URI autorisés doit être conforme aux normes proposées dans la norme RFC 3987 - des identificateurs de ressource (IRIs). Caractères identifiés comme réservés dans RFC 3986 ne doit être % codée. . Noms de fichier ne doit contenir aucun des caractères suivants : \ / : ? \<\> | « ou \*.  
  
## <a name="appendix-a---uri-scheme-registration-template-for-ms-word-scheme"></a>ANNEXE A - MODÈLE URI JEU D’ENREGISTREMENT MODÈLE POUR MS-WORD
<a name="bk_addresources"> </a>

### <a name="a-3-uri-scheme-syntax"></a>A-3. Syntaxe d’URI de schéma

> Modèle Word = « ms-word : « ouvrir pour modification cmd | cmd ouvert pour affichage | nouvelle-de-modèle-cmd
    
> Ouvrir pour modification cmd = « dese | u | « uri de document
    
> ouvert pour affichage cmd = « complément | u | « uri de document
    
> nouvelle-de-modèle-cmd = « nft | u | « modèle uri [ » | s | « enregistrer-emplacement]
    
> uri de document = emplacement URI du document à ouvrir
    
> modèle uri = emplacement de l’URI du fichier de modèle sur lequel le nouveau fichier sera basée
    
> emplacement de sauvegarde = emplacement de l’URI du dossier dans lequel le nouveau document doit être créé
    
### <a name="a-4-uri-scheme-semantics"></a>A-4. Sémantique de schéma URI

Le jeu de ms-word définit une syntaxe d’URI d’ouverture ou de création d’un document de traitement de texte. Le schéma définit trois commandes qui servent à obtenir des instructions concernant ce qui doit être effectué avec le document référencé. Les commandes sont 1) Ouvrir-pour-modifier-cmd (dese), qui demande à une application de traitement de texte pour ouvrir le document à l’URI spécifié pour modification ; (2) Ouvrir-pour-affichage-cmd (complément), qui demande à une application de traitement de texte pour ouvrir le document à l’URI spécifié en mode lecture seule ; et 3) nouvelle-de-modèle-cmd (nft), qui demande à une application de traitement de texte pour créer un nouveau document basé sur le modèle de document à l’URI de l’uri de modèle spécifié et enregistrez le nouveau document dans l’emplacement spécifié dans l’option URI de l’emplacement de l’enregistrement ou, en l’absence de cet URI facultatif, à l’emplacement de bibliothèque de documents par défaut.
  
### <a name="a-5-applicationsprotocols-that-use-the-ms-word-uri-scheme"></a>A-5. Protocoles applications qui utilisent le modèle URI ms-word

Le modèle d’URI ms-word est utilisé par Microsoft Office 2013 pour invoquer Microsoft Word 2013 ou Microsoft Word 2010 avec Service Pack 2. Microsoft SharePoint 2013 utilise ms-word URI sous forme de liens à des documents de traitement de texte stockées dans des bibliothèques de documents SharePoint.
  
### <a name="a-6-interoperability-considerations"></a>A-6. Considérations relatives à l’interopérabilité

Notez que la barre verticale est utilisée comme séparateur dans cette spécification n’est pas entre ces caractères identifiés dans la section 2.2 de RFC 3986 comme réservée à un usage potentiels comme séparateurs... Cette opération est effectuée intentionnellement afin d’optimiser le jeu de caractères, l’URI argument de commande peut prendre en charge sans avoir à coder pour cent ces caractères.
  
Dans < *argument de commande* > segments les caractères réservés RFC 3986 « : » et « / » font partie des données argument, pas les délimiteurs et sont par conséquent inclus sans séquence d’échappement. 
  
### <a name="a-7-security-considerations"></a>A-7. Aspects relatifs à la sécurité

 Sur les systèmes qui se sont inscrits pour reconnaître et agir sur ms-word gestionnaires d’URI, en cliquant sur un lien vers un URI ms-word entraînera l’application de traitement inscrits à être lancé, avec des instructions pour l’application pour essayer d’ouvrir un document de traitement de texte à l’URI spécifié. Les applications de traitement de texte inscription pour traiter ms-word URI doivent implémenter les protections pour vous protéger contre l’ouverture de documents à partir des systèmes distants non fiables qui peuvent contenir du code malveillant. 
  
### <a name="a-8-references"></a>A-8. Références

RFC 3987 - International IRI (Resource Identifiers)  
  
## <a name="appendix-b---uri-scheme-registration-template-for-ms-powerpoint-scheme"></a>ANNEXE B - LE MODÈLE POUR MS-POWERPOINT MODÈLE URI JEU D’ENREGISTREMENT
<a name="bk_addresources"> </a>

### <a name="b-3-uri-scheme-syntax"></a>B-3. Syntaxe d’URI de schéma

- Jeu de PowerPoint = « ms-powerpoint : « ouvrir pour modification cmd | cmd ouvert pour affichage | nouvelle-de-modèle-cmd
    
- Ouvrir pour modification cmd = « dese | u | « uri de document
    
- ouvert pour affichage cmd = « complément | u | « uri de document
    
- nouvelle-de-modèle-cmd = « nft | u | « modèle uri [ » | s | « enregistrer-emplacement]
    
- uri de document = emplacement URI du document à ouvrir
    
- modèle uri = emplacement de l’URI du fichier de modèle sur lequel le nouveau fichier sera basée
    
- emplacement de l’enregistrement\* = emplacement de l’URI du dossier dans lequel le nouveau document doit être créé
    
- \*emplacement de l’enregistrement est un paramètre facultatif
    
### <a name="b-4-uri-scheme-semantics"></a>B-4. Sémantique de schéma URI

Le jeu de ms-powerpoint définit une syntaxe d’URI d’ouverture ou de création d’un document de présentation. Le schéma définit trois commandes qui servent à obtenir des instructions concernant ce qui doit être effectué avec le document référencé. Les commandes sont 1) Ouvrir-pour-modifier-cmd (dese), qui demande à une application de présentation pour ouvrir le document à l’URI spécifié pour modification ; (2) Ouvrir-pour-affichage-cmd (complément), qui demande à une application de présentation pour ouvrir le document à l’URI spécifié en mode lecture seule ; et 3) nouvelle-de-modèle-cmd (nft), qui demande à une application de présentation pour créer un nouveau document basé sur le modèle de document à l’URI de l’uri de modèle spécifié et enregistrez le nouveau document dans l’emplacement spécifié dans l’option URI de l’emplacement de l’enregistrement ou, en l’absence de cet URI facultatif, à l’emplacement de bibliothèque de documents par défaut.
  
### <a name="b-5-applicationsprotocols-that-use-the-ms-powerpoint-uri-scheme"></a>B-5. Protocoles applications qui utilisent le modèle URI ms-powerpoint

Le modèle URI ms-powerpoint est utilisé par Microsoft Office 2013 pour invoquer Microsoft PowerPoint 2013 ou Microsoft PowerPoint 2010 avec Service Pack 2. Microsoft SharePoint 2013 utilise ms-powerpoint URI sous forme de liens sur présentation des documents stockés dans des bibliothèques de documents SharePoint.
  
### <a name="b-6-interoperability-considerations"></a>B-6. Considérations relatives à l’interopérabilité

Notez que la barre verticale est utilisée comme séparateur dans cette spécification n’est pas entre ces caractères identifiés dans la section 2.2 de RFC 3986 comme réservée à un usage potentiels comme séparateurs. Cette opération est effectuée intentionnellement afin d’optimiser le jeu de caractères, l’URI argument de commande peut prendre en charge sans avoir à coder pour cent ces caractères.
  
Dans < *argument de commande* > segments les caractères réservés RFC 3986 « : » et « / » font partie des données argument, pas les délimiteurs et sont par conséquent inclus sans séquence d’échappement. 
  
### <a name="b-7-security-considerations"></a>B-7. Aspects relatifs à la sécurité

Sur les systèmes qui se sont inscrits pour reconnaître et agir sur ms-powerpoint gestionnaires d’URI, en cliquant sur un lien vers un URI ms-powerpoint entraînera l’application de présentation inscrits à lancer, avec des instructions pour l’application pour essayer d’ouvrir un document à l’URI spécifié. Applications inscription pour traiter ms-powerpoint URI doivent implémenter les protections pour vous protéger contre l’ouverture de documents à partir des systèmes distants non fiables qui peuvent contenir du code malveillant.
  
### <a name="b-8-references"></a>B-8. Références

RFC 3987 - International IRI (Resource Identifiers)  
  
## <a name="appendix-c---uri-scheme-registration-template-for-ms-excel-scheme"></a>ANNEXE C : LE MODÈLE POUR MS-EXCEL MODÈLE URI JEU D’ENREGISTREMENT
<a name="bk_addresources"> </a>

### <a name="c-3-uri-scheme-syntax"></a>C-3. Syntaxe d’URI de schéma

> Modèle Excel = « ms-excel : « ouvrir pour modification cmd | cmd ouvert pour affichage | nouvelle-de-modèle-cmd
    
> Ouvrir pour modification cmd = « dese | u | « uri de document
    
> ouvert pour affichage cmd = « complément | u | « uri de document
    
> nouvelle-de-modèle-cmd = « nft | u | « modèle uri [ » | s | « enregistrer-emplacement]
    
> uri de document = emplacement URI du document à ouvrir
    
> modèle uri = emplacement de l’URI du fichier de modèle sur lequel le nouveau fichier sera basée
    
> emplacement de l’enregistrement\* = emplacement de l’URI du dossier dans lequel le nouveau document doit être créé
    
> \*emplacement de l’enregistrement est un paramètre facultatif
    
### <a name="c-4-uri-scheme-semantics"></a>C-4. Sémantique de schéma URI

Le jeu de ms-excel définit une syntaxe d’URI d’ouverture ou de création d’un document de feuille de calcul. Le schéma définit trois commandes qui servent à obtenir des instructions concernant ce qui doit être effectué avec le document référencé. Les commandes sont 1) Ouvrir-pour-modifier-cmd (dese), qui demande à une application de feuilles de calcul pour ouvrir le document à l’URI spécifié pour modification ; (2) Ouvrir-pour-affichage-cmd (complément), qui demande à une application de feuilles de calcul pour ouvrir le document à l’URI spécifié en mode lecture seule ; et 3) nouvelle-de-modèle-cmd (nft), qui demande à une application de feuilles de calcul pour créer un nouveau document basé sur le modèle de document à l’URI de l’uri de modèle spécifié et enregistrez le nouveau document dans l’emplacement spécifié dans l’option URI de l’emplacement de l’enregistrement ou, en l’absence de cet URI facultatif, à l’emplacement de bibliothèque de documents par défaut.
  
### <a name="c-5-applicationsprotocols-that-use-the-ms-excel-uri-scheme"></a>C-5. Protocoles applications qui utilisent le modèle URI ms-excel

Le ms-excel modèle URI est utilisé par Microsoft Office 2013 pour invoquer Microsoft Excel 2013 ou Microsoft Excel 2010 avec Service Pack 2. Microsoft SharePoint 2013 utilise ms-excel URI sous forme de liens vers des feuilles de calcul documents stockés dans des bibliothèques de documents SharePoint.
  
### <a name="c-6-interoperability-considerations"></a>C-6. Considérations relatives à l’interopérabilité

Notez que la barre verticale est utilisée comme séparateur dans cette spécification n’est pas entre ces caractères identifiés dans la section 2.2 de RFC 3986 comme réservée à un usage potentiels comme séparateurs. Cette opération est effectuée intentionnellement afin d’optimiser le jeu de caractères, l’URI argument de commande peut prendre en charge sans avoir à coder pour cent ces caractères.
  
Dans < *argument de commande* > segments les caractères réservés RFC 3986 « : » et « / » font partie des données argument, pas les délimiteurs et sont par conséquent inclus sans séquence d’échappement. 
  
### <a name="c-7-security-considerations"></a>C-7. Aspects relatifs à la sécurité

Sur les systèmes qui ont inscrit des gestionnaires pour reconnaître et agir sur ms-excel URI, en cliquant sur un lien vers un ms-excel URI entraîne l’application des feuilles de calcul à utiliser, avec des instructions pour l’application pour essayer d’ouvrir un document spécifié URI. Inscription au processus des applications excel ms URI doit implémenter les protections pour vous protéger contre l’ouverture de documents à partir des systèmes distants non fiables qui peuvent contenir du code malveillant.
  
### <a name="c-8-references"></a>C-8. Références

RFC 3987 - International IRI (Resource Identifiers)  
  
## <a name="appendix-d---uri-scheme-registration-template-for-ms-visio-scheme"></a>ANNEXE D - MODÈLE DE MS-VISIO POUR MODÈLE URI JEU D’ENREGISTREMENT
<a name="bk_addresources"> </a>

### <a name="d-3-uri-scheme-syntax"></a>D-3. Syntaxe d’URI de schéma

> Jeu de Visio = « ms-visio : « ouvrir pour modification cmd | cmd ouvert pour affichage | nouvelle-de-modèle-cmd
    
> Ouvrir pour modification cmd = « dese | u | « uri de document
    
> ouvert pour affichage cmd = « complément | u | « uri de document
    
> nouvelle-de-modèle-cmd = « nft | u | « modèle uri [ » | s | « enregistrer-emplacement]
    
> uri de document = emplacement URI du document à ouvrir
    
> modèle uri = emplacement de l’URI du fichier de modèle sur lequel le nouveau fichier sera basée
    
> emplacement de l’enregistrement\* = emplacement de l’URI du dossier dans lequel le nouveau document doit être créé
    
> \*emplacement de l’enregistrement est un paramètre facultatif
    
### <a name="d-4-uri-scheme-semantics"></a>D-4. Sémantique de schéma URI

Le jeu de ms-visio définit une syntaxe d’URI d’ouverture ou de création d’un document Microsoft Visio. Le schéma définit trois commandes qui servent à obtenir des instructions concernant ce qui doit être effectué avec le document référencé. Les commandes sont 1) Ouvrir-pour-modifier-cmd (dese), qui demande à Visio pour ouvrir le document à l’URI spécifié pour modification ; (2) Ouvrir-pour-affichage-cmd (complément), qui demande à Visio pour ouvrir le document à l’URI spécifié en mode lecture seule ; et 3) nouvelle-de-modèle-cmd (nft), qui demande à Visio de créer un nouveau document basé sur le modèle de document à l’URI de l’uri de modèle spécifié et enregistrez le nouveau document soit à l’emplacement spécifié dans l’URI de l’option Enregistrer-emplacement ou, dans la absence de cet URI facultatif, à l’emplacement de bibliothèque de documents par défaut.
  
### <a name="d-5-applicationsprotocols-that-use-the-ms-visio-uri-scheme"></a>D-5. Protocoles applications qui utilisent le modèle URI ms-visio

Le modèle d’URI ms-visio est utilisé par Microsoft Office 2013 pour invoquer Microsoft Visio 2013 ou Microsoft Visio 2010 avec Service Pack 2. Microsoft SharePoint 2013 utilise ms-visio URI sous forme de liens aux documents Visio stockés dans des bibliothèques de documents SharePoint.
  
### <a name="d-6-interoperability-considerations"></a>D-6. Considérations relatives à l’interopérabilité

Notez que la barre verticale est utilisée comme séparateur dans cette spécification n’est pas entre ces caractères identifiés dans la section 2.2 de RFC 3986 comme réservée à un usage potentiels comme séparateurs. Cette opération est effectuée intentionnellement afin d’optimiser le jeu de caractères, l’URI argument de commande peut prendre en charge sans avoir à coder pour cent ces caractères.
  
Dans < *argument de commande* > segments les caractères réservés RFC 3986 « : » et « / » font partie des données argument, pas les délimiteurs et sont par conséquent inclus sans séquence d’échappement. 
  
### <a name="d-7-security-considerations"></a>D-7. Aspects relatifs à la sécurité

Sur les systèmes qui se sont inscrits pour reconnaître et agir sur ms-visio gestionnaires d’URI, en cliquant sur un lien vers un URI ms-visio entraîne l’application enregistrée à utiliser, avec des instructions pour l’application pour essayer d’ouvrir un document à l’URI spécifié. Applications inscription pour traiter ms-visio URI doivent implémenter les protections pour vous protéger contre l’ouverture de documents à partir des systèmes distants non fiables qui peuvent contenir du code malveillant.
  
### <a name="d-8-references"></a>D-8. Références

RFC 3987 - International IRI (Resource Identifiers)
  
## <a name="appendix-e---uri-scheme-registration-template-for-ms-access-scheme"></a>ANNEXE E - LE MODÈLE POUR MS-ACCESS MODÈLE URI JEU D’ENREGISTREMENT
<a name="bk_addresources"> </a>

### <a name="e-3-uri-scheme-syntax"></a>E-3. Syntaxe d’URI de schéma

> Accéder jeu = « ms-access : « cmd ouvrir pour modification | cmd ouvert pour affichage | nouvelle-de-modèle-cmd
    
> Ouvrir pour modification cmd = « dese | u | « uri de document
    
> ouvert pour affichage cmd = « complément | u | « uri de document
    
> nouvelle-de-modèle-cmd = « nft | u | « modèle uri [ » | s | « enregistrer-emplacement]
    
> uri de document = emplacement URI du document à ouvrir
    
> modèle uri = emplacement de l’URI du fichier de modèle sur lequel le nouveau fichier sera basée
    
> emplacement de l’enregistrement\* = emplacement de l’URI du dossier dans lequel le nouveau document doit être créé
    
> \*emplacement de l’enregistrement est un paramètre facultatif
    
### <a name="e-4-uri-scheme-semantics"></a>E-4. Sémantique de schéma URI

Le modèle ms-access définit une syntaxe d’URI pour l’ouverture ou la création d’une base de données. Le modèle définit trois commandes qui font office d’instructions concernant les actions à effectuer avec le fichier de base de données. Les commandes sont 1) commande-ouvrir-pour-édition (ofe), qui donne l’instruction à l’application de base de données d’ouvrir la base de données située à l’URI spécifié pour édition ; 2) commande-ouvrir-pour-affichage (ofv), qui donne l’instruction à l’application de base de données d’ouvrir la base de données située à l’URI spécifié en mode lecture seule ; et 3) commande-créer-à-partir-d’un-modèle (nft), qui donne l’instruction à l’application de base de données de créer une base de données basée sur le modèle prédéfini situé à l’URI uri-du-modèle spécifié et d’enregistrer la nouvelle base de données dans l’emplacement spécifié dans l’URI emplacement-d’enregistrement facultatif ou, si cet URI facultatif n’a pas été spécifié, à l’emplacement de la bibliothèque de documents par défaut.
  
### <a name="e-5-applicationsprotocols-that-use-the-ms-access-uri-scheme"></a>E-5. Protocoles applications qui utilisent le modèle URI ms-access

Le modèle URI ms-access est utilisé par Microsoft Office 2013 pour invoquer Microsoft Access 2013 ou Microsoft Access 2010 avec Service Pack 2 à partir de pages web. Microsoft SharePoint 2013 utilise ms-access URI sous forme de liens vers des bases de données Access stockées dans des bibliothèques de documents SharePoint.
  
### <a name="e-6-interoperability-considerations"></a>E-6. Considérations relatives à l’interopérabilité

Notez que la barre verticale est utilisée comme séparateur dans cette spécification n’est pas entre ces caractères identifiés dans la section 2.2 de RFC 3986 comme réservée à un usage potentiels comme séparateurs. Cette opération est effectuée intentionnellement afin d’optimiser le jeu de caractères, l’URI argument de commande peut prendre en charge sans avoir à coder pour cent ces caractères. Dans \<argument de la commande\> segments la RFC 3986 des caractères réservés « : » et « / » font partie des données argument, pas les délimiteurs et sont par conséquent inclus sans séquence d’échappement.
  
### <a name="e-7-security-considerations"></a>E-7. Aspects relatifs à la sécurité

Sur les systèmes qui ont inscrit des gestionnaires pour reconnaître et agir sur ms-access URI, en cliquant sur un lien vers un URI ms-access entraîne l’application enregistrée à utiliser, avec des instructions pour l’application pour essayer d’ouvrir une base de données à l’URI spécifié. Applications inscription pour traiter ms-access URI doivent implémenter les protections pour vous protéger contre l’ouverture des bases de données à partir des systèmes distants non fiables qui peuvent contenir du code malveillant.
  
### <a name="e-8-references"></a>E-8. Références

RFC 3987 - International IRI (Resource Identifiers)  
  
## <a name="appendix-f---uri-scheme-registration-template-for-ms-project-scheme"></a>ANNEXE F - LE MODÈLE POUR MS-PROJET MODÈLE URI JEU D’ENREGISTREMENT
<a name="bk_addresources"> </a>

### <a name="f-3-uri-scheme-syntax"></a>F-3. Syntaxe d’URI de schéma

> Modèle de projet = « ms project : « cmd ouvrir pour modification | cmd ouvert pour affichage | nouvelle-de-modèle-cmd
    
> Ouvrir pour modification cmd = « dese | u | « uri de document
    
> ouvert pour affichage cmd = « complément | u | « uri de document
    
> nouvelle-de-modèle-cmd = « nft | u | « modèle uri [ » | s | « enregistrer-emplacement]
    
> uri de document = emplacement URI du document à ouvrir
    
> modèle uri = emplacement de l’URI du fichier de modèle sur lequel le nouveau fichier sera basée
    
> emplacement de l’enregistrement\* = emplacement de l’URI du dossier dans lequel le nouveau document doit être créé
    
> \*emplacement de l’enregistrement est un paramètre facultatif
    
### <a name="f-4-uri-scheme-semantics"></a>F-4. Sémantique de schéma URI

Le jeu de ms project définit une syntaxe d’URI d’ouverture ou de création d’un document Microsoft Project. Le schéma définit trois commandes qui servent à obtenir des instructions concernant ce qui doit être effectué avec le document référencé. Les commandes sont 1) Ouvrir-pour-modifier-cmd (dese), qui indique à Project pour ouvrir le document à l’URI spécifié pour modification ; (2) Ouvrir-pour-affichage-cmd (complément), qui indique à Project pour ouvrir le document à l’URI spécifié en mode lecture seule ; et 3) nouvelle-de-modèle-cmd (nft), qui indique à Project pour créer un nouveau document basé sur le modèle de document à l’URI de l’uri de modèle spécifié et enregistrez le nouveau document soit à l’emplacement spécifié dans l’URI de l’option Enregistrer-emplacement ou, dans la absence de cet URI facultatif, à l’emplacement de bibliothèque de documents par défaut.
  
### <a name="f-5-applicationsprotocols-that-use-the-ms-project-uri-scheme"></a>F-5. Protocoles applications qui utilisent le modèle URI ms project

Le modèle URI ms-projet est utilisé par Microsoft Office 2013 pour invoquer Microsoft Project 2013 à partir des pages web. Microsoft SharePoint 2013 utilise ms-projet URI sous forme de liens à des documents de projet stockées dans les bibliothèques de documents SharePoint.
  
### <a name="f-6-interoperability-considerations"></a>F-6. Considérations relatives à l’interopérabilité

Notez que la barre verticale est utilisée comme séparateur dans cette spécification n’est pas entre ces caractères identifiés dans la section 2.2 de RFC 3986 comme réservée à un usage potentiels comme séparateurs. Cette opération est effectuée intentionnellement afin d’optimiser le jeu de caractères, l’URI argument de commande peut prendre en charge sans avoir à coder pour cent ces caractères.
  
Dans < *argument de commande* > segments les caractères réservés RFC 3986 « : » et « / » font partie des données argument, pas les délimiteurs et sont par conséquent inclus sans séquence d’échappement. 
  
### <a name="f-7-security-considerations"></a>F-7. Aspects relatifs à la sécurité

Sur les systèmes qui ont inscrit des gestionnaires pour reconnaître et agir sur ms-projet URI, en cliquant sur un lien vers un URI ms-projet entraîne l’application enregistrée à utiliser, avec des instructions pour l’application pour essayer d’ouvrir un document à l’URI spécifié. Applications inscription pour traiter les projets ms URI doivent implémenter les protections pour vous protéger contre l’ouverture de documents à partir des systèmes distants non fiables qui peuvent contenir du code malveillant.
  
### <a name="f-8-references"></a>F-8. Références

RFC 3987 - International IRI (Resource Identifiers)  
  
## <a name="appendix-g---uri-scheme-registration-template-for-ms-publisher-scheme"></a>ANNEXE G - LE MODÈLE POUR MS-PUBLISHER MODÈLE URI JEU D’ENREGISTREMENT
<a name="bk_addresources"> </a>

### <a name="g-3-uri-scheme"></a>G-3. Modèle URI

> Modèle de Publisher syntaxe = « ms-publisher : « cmd ouvrir pour modification | cmd ouvert pour affichage | nouvelle-de-modèle-cmd
    
> Ouvrir pour modification cmd = « dese | u | « uri de document
    
> ouvert pour affichage cmd = « complément | u | « uri de document
    
> nouvelle-de-modèle-cmd = « nft | u | « modèle uri [ » | s | « enregistrer-emplacement]
    
> uri de document = emplacement URI du document à ouvrir
    
> modèle uri = emplacement de l’URI du fichier de modèle sur lequel le nouveau fichier sera basée
    
> emplacement de l’enregistrement\* = emplacement de l’URI du dossier dans lequel le nouveau document doit être créé
    
> \*emplacement de l’enregistrement est un paramètre facultatif
    
### <a name="g-4-uri-scheme-semantics"></a>G-4. Sémantique de schéma URI

Le modèle ms-publisher définit une syntaxe d’URI pour l’ouverture ou la création d’un document Microsoft Publisher. Le modèle définit trois commandes qui font office d’instructions concernant les actions à effectuer avec le document référencé. Les commandes sont 1) commande-ouvrir-pour-édition (ofe), qui donne l’instruction à Publisher d’ouvrir le document situé à l’URI spécifié pour édition ; 2) commande-ouvrir-pour-affichage (ofv), qui donne l’instruction à Publisher d’ouvrir le document situé à l’URI spécifié en mode lecture seule ; et 3) commande-créer-à-partir-d’un-modèle (nft), qui donne l’instruction à Publisher de créer un document basé sur le modèle prédéfini de document situé à l’URI uri-du-modèle spécifié et d’enregistrer le nouveau document dans l’emplacement spécifié dans l’URI emplacement-d’enregistrement facultatif ou, si cet URI facultatif n’a pas été spécifié, à l’emplacement de la bibliothèque de documents par défaut.
  
### <a name="g-5-applicationsprotocols-that-use-the-ms-publisher-uri-scheme"></a>G-5. Protocoles applications qui utilisent le modèle URI ms-publisher

Le modèle URI ms-publisher est utilisé par Microsoft Office 2013 pour invoquer Microsoft Publisher 2013 ou Microsoft Publisher 2010 avec Service Pack 2 à partir de pages web. Microsoft SharePoint 2013 utilise ms-publisher URI sous forme de liens aux documents Publisher stockés dans des bibliothèques de documents SharePoint.
  
### <a name="g-6-interoperability-considerations"></a>G-6. Considérations relatives à l’interopérabilité

Notez que la barre verticale est utilisée comme séparateur dans cette spécification n’est pas entre ces caractères identifiés dans la section 2.2 de RFC 3986 comme réservée à un usage potentiels comme séparateurs. Cette opération est effectuée intentionnellement afin d’optimiser le jeu de caractères, l’URI argument de commande peut prendre en charge sans avoir à coder pour cent ces caractères. Dans \<argument de la commande\> segments la RFC 3986 des caractères réservés « : » et « / » font partie des données argument, pas les délimiteurs et sont par conséquent inclus sans séquence d’échappement.
  
### <a name="g-7-security-considerations"></a>G-7. Aspects relatifs à la sécurité

Sur les systèmes qui ont enregistré des gestionnaires pour reconnaître et effectuer les actions des URI ms-publisher, le fait de cliquer sur un lien vers un URI ms-publisher entraîne le lancement de l’application enregistrée, avec des instructions pour que l’application tente d’ouvrir un document situé à l’URI spécifié. Les applications enregistrées pour traiter des URI ms-publisher doivent mettre en œuvre des protections pour empêcher l’ouverture de documents provenant de systèmes distants non approuvés pouvant inclure du code malveillant.
  
### <a name="g-9-references"></a>G-9. Références

RFC 3987 - International IRI (Resource Identifiers)  
  
## <a name="appendix-h---uri-scheme-registration-template-for-ms-spd-scheme"></a>ANNEXE H - LE MODÈLE POUR MS-SPD MODÈLE URI JEU D’ENREGISTREMENT
<a name="bk_addresources"> </a>

### <a name="h-3-uri-scheme-syntax"></a>H-3. Syntaxe d’URI de schéma

> SharePoint Designer jeu = « ms-spd : « cmd ouvrir pour modification
    
> Ouvrir pour modification cmd = « dese | u | « uri de document
    
> uri de document = emplacement URI du document à ouvrir
    
### <a name="h-4-uri-scheme-semantics"></a>H-4. Sémantique de schéma URI

Le jeu de ms-spd définit une syntaxe d’URI pour l’ouverture d’un document Microsoft SharePoint Designer. Le schéma définit deux commandes qui servent à obtenir des instructions concernant ce qui doit être effectué avec le document référencé. Les commandes sont 1) Ouvrir-pour-modifier-cmd (dese), qui indique à SharePoint Designer pour ouvrir le document à l’URI spécifié pour modification ; et 2) Ouvrir-pour-affichage-cmd (complément), qui indique à SharePoint Designer pour ouvrir le document à l’URI spécifié en mode lecture seule.
  
### <a name="h-5-applicationsprotocols-that-use-the-ms-spd-uri-scheme"></a>H-5. Protocoles applications qui utilisent le modèle URI ms-spd

Le modèle d’URI ms-spd est utilisé par Microsoft Office 2013 pour invoquer Microsoft SharePoint Designer 2013 à partir des pages web. Microsoft SharePoint 2013 utilise ms-spd URI sous forme de liens à SharePoint Designer des documents stockés dans des bibliothèques de documents SharePoint.
  
### <a name="h-6-interoperability-considerations"></a>H-6. Considérations relatives à l’interopérabilité

Notez que la barre verticale est utilisée comme séparateur dans cette spécification n’est pas entre ces caractères identifiés dans la section 2.2 de RFC 3986 comme réservée à un usage potentiels comme séparateurs. Cette opération est effectuée intentionnellement afin d’optimiser le jeu de caractères, l’URI argument de commande peut prendre en charge sans avoir à coder pour cent ces caractères.
  
Dans < *argument de commande* > segments les caractères réservés RFC 3986 « : » et « / » font partie des données argument, pas les délimiteurs et sont par conséquent inclus sans séquence d’échappement. 
  
### <a name="h-7-security-considerations"></a>H-7. Aspects relatifs à la sécurité

Sur les systèmes qui se sont inscrits pour reconnaître et agir sur ms-spd gestionnaires d’URI, en cliquant sur un lien vers un URI ms-spd entraîne l’application enregistrée à utiliser, avec des instructions pour l’application pour essayer d’ouvrir un document à l’URI spécifié. Applications inscription pour traiter ms-spd URI doivent implémenter les protections pour vous protéger contre l’ouverture de documents à partir des systèmes distants non fiables qui peuvent contenir du code malveillant.
  
### <a name="h-8-references"></a>H-8. Références

RFC 3987 - International IRI (Resource Identifiers)  
  
## <a name="appendix-i---uri-scheme-registration-template-for-ms-infopath-scheme"></a>ANNEXE I - LE MODÈLE POUR MS-INFOPATH MODÈLE URI JEU D’ENREGISTREMENT
<a name="bk_addresources"> </a>

###   <a name="i-3-uri-scheme-syntax"></a>I-3. Syntaxe d’URI de schéma

> Schéma InfoPath = « ms-infopath : « ouvrir pour modification cmd | Ouvrir pour afficher cmd
    
> Ouvrir pour modification cmd = « dese | u | « uri de document
    
> ouvert pour affichage cmd = « complément | u | « uri de document
    
> uri de document = emplacement URI du document à ouvrir
    
### <a name="i-4-uri-scheme-semantics"></a>I-4. Sémantique de schéma URI

Le modèle ms-infopath définit une syntaxe d’URI pour l’ouverture ou la création d’un document Microsoft Infopath. Le modèle définit deux commandes qui font office d’instructions concernant les actions à effectuer avec le document référencé. Les commandes sont 1) commande-ouvrir-pour-édition (ofe), qui donne l’instruction à Infopath d’ouvrir le document situé à l’URI spécifié pour édition ; 2) commande-ouvrir-pour-affichage (ofv), qui donne l’instruction à Infopath d’ouvrir le document situé à l’URI spécifié en mode lecture seule
  
### <a name="i-5-applicationsprotocols-that-use-the-ms-infopath-uri-scheme"></a>I-5. Protocoles applications qui utilisent le modèle URI ms-infopath

Le modèle d’URI ms-infopath est utilisé par Microsoft Office 2013 pour appeler Microsoft Infopath 2013 à partir de pages web. Microsoft SharePoint 2013 utilise les URI ms-infopath comme des liens vers des documents Infopath stockés dans des bibliothèques de documents SharePoint.
  
### <a name="i-6-interoperability-considerations"></a>I-6. Considérations relatives à l’interopérabilité

Notez que la barre verticale est utilisée comme séparateur dans cette spécification n’est pas entre ces caractères identifiés dans la section 2.2 de RFC 3986 comme réservée à un usage potentiels comme séparateurs. Cette opération est effectuée intentionnellement afin d’optimiser le jeu de caractères, l’URI argument de commande peut prendre en charge sans avoir à coder pour cent ces caractères.
  
Dans < *argument de commande* > segments les caractères réservés RFC 3986 « : » et « / » font partie des données argument, pas les délimiteurs et sont par conséquent inclus sans séquence d’échappement. 
  
### <a name="i-7-security-considerations"></a>I-7. Aspects relatifs à la sécurité

Sur les systèmes qui ont inscrit des gestionnaires pour reconnaître et agir sur ms-infopath URI, en cliquant sur un lien vers un URI ms-infopath entraîne l’application enregistrée à utiliser, avec des instructions pour l’application pour essayer d’ouvrir un document à l’URI spécifié. Applications inscription pour traiter ms-infopath URI doivent implémenter les protections pour vous protéger contre l’ouverture de documents à partir des systèmes distants non fiables qui peuvent contenir du code malveillant.
  
### <a name="i-8-references"></a>I-8. Références

RFC 3987 - International IRI (Resource Identifiers)  
  

