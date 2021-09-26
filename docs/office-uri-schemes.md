---
title: Modèles d’URI Office
manager: luken
ms.date: 01/14/2016
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 1ea99a8f-b005-4b92-b313-923294d20fbf
ms.openlocfilehash: cd6f55f5727782bae5880f89bb983c08db413a4f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611048"
---
# <a name="office-uri-schemes"></a>Modèles d’URI Office

## <a name="11-abstract"></a>1.1 RÉSUMÉ

Ce document définit le format des URI (Uniform Resource Identifier) pour les applications de productivité Office. Ce modèle est pris en charge dans Microsoft Office 2010 Service Pack 2 et versions ultérieures, y compris Microsoft Office 2013 pour Windows et les produits Microsoft SharePoint 2013. Il est également pris en charge dans Office pour iPhone, Office pour iPad et Microsoft Office pour Mac 2011.
  
## <a name="12-introduction"></a>1.2 INTRODUCTION

Ces modèles d’URI permettent aux applications de productivité Office d’être appelées par différentes commandes. Un modèle nommé différent est attribué à chaque application, mais tous les modèles suivent les mêmes règles de formation de l’URI (modèle d’URI).

  
## <a name="13-uri-schema"></a>1.3 MODÈLE D’URI

### <a name="full-schema"></a>Modèle complet

< *scheme-name*  >:<  *command-name*  >"|"<  *command-argument-descriptor*  > "|"<  *command-argument*  > 
  
Un URI, tel que défini dans ce document, peut comporter un ou plusieurs arguments de commande, qui peuvent chacun contenir les éléments < *command-argument-descriptor* > et < *command-argument* > et être délimités par une barre verticale (« | »). Quand l’URI comporte plusieurs arguments de commande, une barre verticale (« | ») doit délimiter chaque argument de commande de l’argument suivant. 
  
Ces modèles ne contiennent pas de composant d’autorité comme défini dans la section 3.2 du RFC 3986. Les commandes spécifiées dans ce document sont appelées quand le système appelle la commande. Par exemple, quand l’URI « ms-excel:ofv|u|https://contoso/Q4/budget.xls » est appelé à partir d’un ordinateur personnel exécutant Microsoft Windows doté de Microsoft Office 2013, l’application locale Microsoft Excel est généralement lancée et transmet les arguments pour ouvrir ce fichier dans  *https://contoso/Q4/budget.xls*  en lecture seule. Notez que la barre verticale utilisée comme délimiteur dans cette spécification ne fait pas partie des caractères identifiés à la section 2.2 du RFC 3986 qui sont réservés à un usage éventuel comme délimiteurs. Cette opération vise à optimiser le jeu de caractères que l’argument de commande de l’URI peut prendre en charge sans avoir à coder ces caractères en pourcentage. 
  
La syntaxe du modèle inclut les éléments suivants :
  
1. < *scheme-name*  > : type de l’application à appeler. Par exemple, le nom de modèle ms-word: est déposé par Microsoft Word. 
    
2. Délimiteur « : »
    
3. < *command-name*  > : décrit les actions que l’application doit effectuer. Par exemple, ouvrir un document pour le consulter. La liste des noms de commande figure à la section 1.5. 
    
4. Délimiteur « | » (barre verticale)
    
5. < *command-argument-descriptor*  > : cet élément fournit davantage d’informations sur l’objet de l’argument de commande. 
    
6. Délimiteur « | » (barre verticale)
    
7. < *command-argument*  > : les arguments varient en fonction de la commande. L’URI vers un document est un argument courant qui utilise généralement le modèle http ou https. Notez que, dans les segments <  *command-argument*  >, les caractères réservés dans le document RFC 3986 « : » et « / » font partie des données d’argument mais ne sont pas des délimiteurs, et sont donc inclus sans séquence d’échappement. 
    
### <a name="abbreviated-schema"></a>Modèle abrégé

Une forme abrégée des modèles d’URI Office permet à une demande plus compacte de lancer une application Office spécifiée pour ouvrir la ressource située à un URI donné. Cette forme abrégée indique les éléments < < *command-name*  > "ofv" et <  *command-argument-descriptor*  > "u". Aucune commande, ni aucun argument de commande, n’est autorisé dans ce schéma. 
  
< *scheme-name*  >:<  *command-argument*  > 
  
1. < *scheme-name*  > : type de l’application à appeler. Par exemple, ms-word: pour Microsoft Word. 
    
2. < *command-argument*  > : URI de la ressource que l’application doit ouvrir. Actuellement, seuls les URI basés sur le modèle http ou https sont pris en charge. 
    
## <a name="14-scheme-names-and-office-application-registrations"></a>1.4 NOM DES MODÈLES ET ENREGISTREMENT DES APPLICATIONS OFFICE

Voici la liste des noms de modèles implémentés dans les applications Microsoft Office. Quand Microsoft Office est installé, chaque nom de modèle est enregistré dans Windows pour être géré par le produit Office du même nom. Notez que « ms-spd » est une abréviation de SharePoint Designer.
  
> - *ms-word:* 
    
> - *ms-powerpoint:* 
    
> - *ms-excel:* 
    
> - *ms-visio:* 
    
> - *ms-access:* 
    
> - *ms-project:* 
    
> - *ms-publisher:* 
    
> - *ms-spd:* 
    
> - *ms-infopath:* 
    
## <a name="15-commands-and-required-command-arguments"></a>1.5 COMMANDES ET ARGUMENTS DE COMMANDE REQUIS

### <a name="view-document"></a>Afficher le document

La commande suivante force l’application à ouvrir le document référencé par l’URI en mode Lecture seule ou Affichage.
  
> Nom de la commande : ofv
    
> Descripteur de l’argument de commande : u
    
> Argument de commande : URI vers le document, construit sur le modèle http ou https
    
> Exemple : *ms-excel:ofv|u|https://contoso/Q4/budget.xls* 
    
### <a name="edit-document"></a>Modifier le document

La commande suivante force l’application à ouvrir le document référencé par l’URI en mode Édition.
  
> Nom de la commande : ofe
    
> Descripteur de l’argument de commande : u
    
> Argument de commande : URI vers le document, construit sur le modèle http ou https
    
> Exemple :  *ms-powerpoint:ofe|u|https://www.fourthcoffee.com/AllHandsDeck.ppt* 
    
### <a name="new-document-from-template"></a>Nouveau document à partir d’un modèle

La commande suivante entraîne l’ouverture et la création par l’application d’un nouveau document basé sur le modèle prédéfini situé à l’URI spécifié. Le fichier de modèle prédéfini n’est pas modifié dans ce processus. Un argument de commande supplémentaire peut être indiqué pour spécifier le chemin d’accès par défaut proposé en tant qu’emplacement d’enregistrement lorsque le fichier est enregistré pour la première fois. L’utilisateur peut cependant choisir un autre emplacement.

  
> Nom de la commande : nft
    
> Descripteur de l’argument de commande 1 : u
    
> Argument de commande 1 : URI vers le modèle, construit sur le modèle http ou https
    
> Descripteur de l’argument de commande 2 : s
    
> Argument de commande facultatif 2 : URI pour spécifier le dossier d’enregistrement par défaut
    
> Exemple :  *ms-word:nft|u|https://cohowinery/templates/elegance.pot|s|https://cohowinery/presentations* 
    
Si l’emplacement d’enregistrement par défaut facultatif est renseigné, il doit pointer vers le même nom d’hôte que le modèle.
  
De plus, les applications SharePoint Designer et InfoPath (qui implémentent les modèles ms-sdp: et ms-infopath:, respectivement) ne prennent pas en charge la fonctionnalité de création d’un nouveau document à partir d’un modèle.
  
## <a name="16-backwards-compatibility"></a>1.6 COMPATIBILITÉ DESCENDANTE


Lors de l’analyse d’un URI pour en extraire les arguments de commande appropriés pour une commande donnée, le gestionnaire d’URI Office utilisera uniquement les arguments de commande présentant le descripteur des arguments de commande attendu. Si des paires d’arguments et des descripteurs d’arguments supplémentaires présentent des descripteurs d’arguments inattendus, ils seront supprimés de l’URI. Ce mécanisme permet aux futures versions du modèle d’ajouter des arguments de commande supplémentaires sans rompre la compatibilité descendante avec des implémentations héritées de ce modèle.

  
## <a name="17-implementation-restrictions-on-command-arguments"></a>1.7 RESTRICTIONS D’IMPLÉMENTATION SUR LES ARGUMENTS DE COMMANDE

Les restrictions suivantes sont placées sur des arguments de commande dans leur implémentation actuelle dans Office 2013.
  
### <a name="length-limitations-on-uri-command-arguments"></a>Limitations de longueur des arguments de commande des URI

Pour les arguments de commande d’URI, la longueur maximale du chemin est de 256 caractères pour toutes les applications, sauf Excel, pour laquelle la limite est de 216. Il est possible que certaines applications prennent en chargent des longueurs des chemins d’accès supérieures à cette limite ; il est recommandé d’effectuer des tests avant de déployer des solutions qui en dépendent.


  
### <a name="allowed-characters-in-uri-command-arguments"></a>Caractères autorisés dans les arguments de commande des URI

Les URI autorisés doivent respecter les normes mentionnées dans le RFC 3987 – Internationalized Resource Identifiers (IRIs). Les caractères identifiés comme étant réservés dans le RFC 3986 ne doivent pas être codés en pourcentage. . Les noms de fichiers ne peuvent pas contenir les caractères suivants : \ / : ? \< \> | " ou \*.  
  
## <a name="appendix-a---uri-scheme-registration-template-for-ms-word-scheme"></a>ANNEXE A – MODÈLE D’ENREGISTREMENT DES MODÈLES D’URI POUR LE MODÈLE MS-WORD
<a name="bk_addresources"> </a>

### <a name="a-3-uri-scheme-syntax"></a>A-3. Syntaxe du modèle d’URI

> Modèle pour Word = "ms-word:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
    
> open-for-edit-cmd = "ofe|u|" document-uri
    
> open-for-view-cmd = "ofv|u|" document-uri
    
> new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]
    
> document-uri = URI d’emplacement du document à ouvrir
    
> template-uri = URI d’emplacement du modèle de fichier sur lequel le nouveau fichier sera basé
    
> save-location = URI d’emplacement du dossier dans lequel le nouveau document doit être créé
    
### <a name="a-4-uri-scheme-semantics"></a>A-4. Sémantique du modèle d’URI

Le modèle ms-word définit une syntaxe d’URI pour l’ouverture ou la création d’un document de traitement de texte. Le modèle définit trois commandes qui font office d’instructions concernant les actions à effectuer avec le document référencé. Les commandes sont 1) commande-ouvrir-pour-édition (ofe), qui donne l’instruction à une application de traitement de texte d’ouvrir le document situé à l’URI spécifié pour édition ; 2) commande-ouvrir-pour-affichage (ofv), qui donne l’instruction à une application de traitement de texte d’ouvrir le document situé à l’URI spécifié en mode lecture seule ; et 3) commande-créer-à-partir-d’un-modèle (nft), qui donne l’instruction à une application de traitement de texte de créer un document basé sur le modèle prédéfini de document situé à l’URI uri-du-modèle spécifié et d’enregistrer le nouveau document dans l’emplacement spécifié dans l’URI emplacement-d’enregistrement facultatif ou, si cet URI facultatif n’a pas été spécifié, à l’emplacement de la bibliothèque de documents par défaut.

  
### <a name="a-5-applicationsprotocols-that-use-the-ms-word-uri-scheme"></a>A-5. Applications/Protocoles qui utilisent le modèle d’URI ms-word

Le modèle d’URI ms-word est utilisé par Microsoft Office 2013 pour appeler Microsoft Word 2013 ou Microsoft Word 2010 avec le Service Pack 2. Microsoft SharePoint 2013 utilise les URI ms-word comme des liens vers des documents de traitement de texte stockés dans des bibliothèques de documents SharePoint.

  
### <a name="a-6-interoperability-considerations"></a>A-6. Considérations relatives à l’interopérabilité

Notez que la barre verticale utilisée comme délimiteur dans cette spécification ne fait pas partie des caractères identifiés à la section 2.2 du RFC 3986 qui sont réservés à un usage éventuel comme délimiteurs. Cette opération vise à optimiser le jeu de caractères que l’argument de commande de l’URI peut prendre en charge sans avoir à coder ces caractères en pourcentage.
  
Dans les segments < *command-argument* >, les caractères réservés dans le document RFC 3986 « : » et « / » font partie des données d’argument mais ne sont pas des délimiteurs, et sont donc inclus sans séquence d’échappement. 
  
### <a name="a-7-security-considerations"></a>A-7. Considérations relatives à la sécurité

 
Sur les systèmes qui ont enregistré des gestionnaires pour reconnaître et effectuer les actions des URI ms-word, le fait de cliquer sur un lien vers un URI ms-word entraîne le lancement de l’application de traitement de texte enregistrée, avec des instructions pour que l’application de traitement de texte tente d’ouvrir un document situé à l’URI spécifié. Les applications de traitement de texte enregistrées pour traiter des URI ms-word doivent mettre en œuvre des protections pour empêcher l’ouverture de documents provenant de systèmes distants non approuvés pouvant inclure du code malveillant.
 
  
### <a name="a-8-references"></a>A-8. Références

RFC 3987 – International Resource Identifiers (IRIs)  
  
## <a name="appendix-b---uri-scheme-registration-template-for-ms-powerpoint-scheme"></a>ANNEXE B – MODÈLE D’ENREGISTREMENT DES MODÈLES D’URI POUR LE MODÈLE MS-POWERPOINT
<a name="bk_addresources"> </a>

### <a name="b-3-uri-scheme-syntax"></a>B-3. Syntaxe du modèle d’URI

- Modèle pour PowerPoint 	= "ms-powerpoint:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
    
- open-for-edit-cmd = "ofe|u|" document-uri
    
- open-for-view-cmd = "ofv|u|" document-uri
    
- new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]
    
- document-uri = URI d’emplacement du document à ouvrir
    
- template-uri = URI d’emplacement du modèle de fichier sur lequel le nouveau fichier sera basé
    
- save-location\* = URI d’emplacement du dossier dans lequel le nouveau document doit être créé
    
- \*save-location est un paramètre facultatif.
    
### <a name="b-4-uri-scheme-semantics"></a>B-4. Sémantique du modèle d’URI

Le modèle ms-powerpoint définit une syntaxe d’URI pour l’ouverture ou la création d’un document de présentation. Le modèle définit trois commandes qui font office d’instructions concernant les actions à effectuer avec le document référencé. Les commandes sont 1) commande-ouvrir-pour-édition (ofe), qui donne l’instruction à une application de présentation d’ouvrir le document situé à l’URI spécifié pour édition ; 2) commande-ouvrir-pour-affichage (ofv), qui donne l’instruction à une application de présentation d’ouvrir le document situé à l’URI spécifié en mode lecture seule ; et 3) commande-créer-à-partir-d’un-modèle (nft), qui donne l’instruction à une application de présentation de créer un document basé sur le modèle prédéfini de document situé à l’URI uri-du-modèle spécifié et d’enregistrer le nouveau document dans l’emplacement spécifié dans l’URI emplacement-d’enregistrement facultatif ou, si cet URI facultatif n’a pas été spécifié, à l’emplacement de la bibliothèque de documents par défaut.

  
### <a name="b-5-applicationsprotocols-that-use-the-ms-powerpoint-uri-scheme"></a>B-5. Applications/Protocoles qui utilisent le modèle d’URI ms-powerpoint

Le modèle d’URI ms-powerpoint est utilisé par Microsoft Office 2013 pour appeler Microsoft PowerPoint 2013 ou Microsoft PowerPoint 2010 avec le Service Pack 2. Microsoft SharePoint 2013 utilise les URI ms-powerpoint comme des liens vers des documents de présentation stockés dans des bibliothèques de documents SharePoint.

  
### <a name="b-6-interoperability-considerations"></a>B-6. Considérations relatives à l’interopérabilité

La barre verticale utilisée comme délimiteur dans cette spécification ne fait pas partie des caractères identifiés à la section 2.2 du document RFC 3986 comme réservés pour être potentiellement utilisés comme délimiteurs. Ceci est intentionnel et permet d’optimiser au maximum le jeu de caractères que l’argument de commande de l’URI peut prendre en charge sans avoir à coder ces caractères en pourcentage. 

  
Dans les segments < *command-argument* >, les caractères réservés dans le document RFC 3986 « : » et « / » font partie des données d’argument mais ne sont pas des délimiteurs, et sont donc inclus sans séquence d’échappement. 
  
### <a name="b-7-security-considerations"></a>B-7. Considérations relatives à la sécurité

Sur les systèmes qui ont enregistré des gestionnaires pour reconnaître et effectuer les actions des URI ms-powerpoint, le fait de cliquer sur un lien vers un URI ms-powerpoint entraîne le lancement de l’application de présentation enregistrée, avec des instructions pour que l’application tente d’ouvrir un document situé à l’URI spécifié. Les applications enregistrées pour traiter des URI ms-powerpoint doivent mettre en œuvre des protections pour empêcher l’ouverture de documents provenant de systèmes distants non approuvés pouvant inclure du code malveillant.

  
### <a name="b-8-references"></a>B-8. Références

RFC 3987 – International Resource Identifiers (IRIs)  
  
## <a name="appendix-c---uri-scheme-registration-template-for-ms-excel-scheme"></a>ANNEXE C – MODÈLE D’ENREGISTREMENT DES MODÈLES D’URI POUR LE MODÈLE MS-EXCEL
<a name="bk_addresources"> </a>

### <a name="c-3-uri-scheme-syntax"></a>C-3. Syntaxe du modèle d’URI

> Modèle pour Excel = "ms-excel:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
    
> open-for-edit-cmd = "ofe|u|" document-uri
    
> open-for-view-cmd = "ofv|u|" document-uri
    
> new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]
    
> document-uri = URI d’emplacement du document à ouvrir
    
> template-uri = URI d’emplacement du modèle de fichier sur lequel le nouveau fichier sera basé
    
> save-location\* = URI d’emplacement du dossier dans lequel le nouveau document doit être créé
    
> \*save-location est un paramètre facultatif.
    
### <a name="c-4-uri-scheme-semantics"></a>C-4. Sémantique du modèle d’URI

Le modèle ms-excel définit une syntaxe d’URI pour l’ouverture ou la création d’une feuille de calcul. Le modèle définit trois commandes qui font office d’instructions concernant les actions à effectuer avec le document référencé. Les commandes sont 1) commande-ouvrir-pour-édition (ofe), qui donne l’instruction à une application de tableur d’ouvrir le document situé à l’URI spécifié pour édition ; 2) commande-ouvrir-pour-affichage (ofv), qui donne l’instruction à une application de tableur d’ouvrir le document situé à l’URI spécifié en mode lecture seule ; et 3) commande-créer-à-partir-d’un-modèle (nft), qui donne l’instruction à une application de tableur de créer un document basé sur le modèle prédéfini de document situé à l’URI uri-du-modèle spécifié et d’enregistrer le nouveau document dans l’emplacement spécifié dans l’URI emplacement-d’enregistrement facultatif ou, si cet URI facultatif n’a pas été spécifié, à l’emplacement de la bibliothèque de documents par défaut.

  
### <a name="c-5-applicationsprotocols-that-use-the-ms-excel-uri-scheme"></a>C-5. Applications/Protocoles qui utilisent le modèle d’URI ms-excel

Le modèle d’URI ms-excel est utilisé par Microsoft Office 2013 pour appeler Microsoft Excel 2013 ou Microsoft Excel 2010 avec le Service Pack 2. Microsoft SharePoint 2013 utilise les URI ms-excel comme des liens vers des feuilles de calcul stockées dans des bibliothèques de documents SharePoint.

  
### <a name="c-6-interoperability-considerations"></a>C-6. Considérations relatives à l’interopérabilité

La barre verticale utilisée comme délimiteur dans cette spécification ne fait pas partie des caractères identifiés à la section 2.2 du document RFC 3986 comme réservés pour être potentiellement utilisés comme délimiteurs. Ceci est intentionnel et permet d’optimiser au maximum le jeu de caractères que l’argument de commande de l’URI peut prendre en charge sans avoir à coder ces caractères en pourcentage. 

  
Dans les segments < *command-argument* >, les caractères réservés dans le document RFC 3986 « : » et « / » font partie des données d’argument mais ne sont pas des délimiteurs, et sont donc inclus sans séquence d’échappement. 
  
### <a name="c-7-security-considerations"></a>C-7. Considérations relatives à la sécurité

Sur les systèmes qui ont enregistré des gestionnaires pour reconnaître et effectuer les actions des URI ms-excel, le fait de cliquer sur un lien vers un URI ms-excel entraîne le lancement de l’application de tableur enregistrée, avec des instructions pour que l’application tente d’ouvrir un document situé à l’URI spécifié. Les applications enregistrées pour traiter des URI ms-excel doivent mettre en œuvre des protections pour empêcher l’ouverture de documents provenant de systèmes distants non approuvés pouvant inclure du code malveillant.

  
### <a name="c-8-references"></a>C-8. Références

RFC 3987 – International Resource Identifiers (IRIs)  
  
## <a name="appendix-d---uri-scheme-registration-template-for-ms-visio-scheme"></a>ANNEXE D – MODÈLE D’ENREGISTREMENT DES MODÈLES D’URI POUR LE MODÈLE MS-VISIO
<a name="bk_addresources"> </a>

### <a name="d-3-uri-scheme-syntax"></a>D-3. Syntaxe du modèle d’URI

> Modèle pour Visio = "ms-visio:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
    
> open-for-edit-cmd = "ofe|u|" document-uri
    
> open-for-view-cmd = "ofv|u|" document-uri
    
> new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]
    
> document-uri = URI d’emplacement du document à ouvrir
    
> template-uri = URI d’emplacement du modèle de fichier sur lequel le nouveau fichier sera basé
    
> save-location\* = URI d’emplacement du dossier dans lequel le nouveau document doit être créé
    
> \*save-location est un paramètre facultatif.
    
### <a name="d-4-uri-scheme-semantics"></a>D-4. Sémantique du modèle d’URI

Le modèle ms-visio définit une syntaxe d’URI pour l’ouverture ou la création d’un document Microsoft Visio. Le modèle définit trois commandes qui font office d’instructions concernant les actions à effectuer avec le document référencé. Les commandes sont 1) commande-ouvrir-pour-édition (ofe), qui donne l’instruction à Visio d’ouvrir le document situé à l’URI spécifié pour édition ; 2) commande-ouvrir-pour-affichage (ofv), qui donne l’instruction à Visio d’ouvrir le document situé à l’URI spécifié en mode lecture seule ; et 3) commande-créer-à-partir-d’un-modèle (nft), qui donne l’instruction à Visio de créer un document basé sur le modèle prédéfini de document situé à l’URI uri-du-modèle spécifié et d’enregistrer le nouveau document dans l’emplacement spécifié dans l’URI emplacement-d’enregistrement facultatif ou, si cet URI facultatif n’a pas été spécifié, à l’emplacement de la bibliothèque de documents par défaut.

  
### <a name="d-5-applicationsprotocols-that-use-the-ms-visio-uri-scheme"></a>D-5. Applications/Protocoles qui utilisent le modèle d’URI ms-visio

Le modèle d’URI ms-visio est utilisé par Microsoft Office 2013 pour appeler Microsoft Visio 2013 ou Microsoft Visio 2010 avec le Service Pack 2. Microsoft SharePoint 2013 utilise les URI ms-visio comme des liens vers des documents Visio stockés dans des bibliothèques de documents SharePoint.

  
### <a name="d-6-interoperability-considerations"></a>D-6. Considérations relatives à l’interopérabilité

La barre verticale utilisée comme délimiteur dans cette spécification ne fait pas partie des caractères identifiés à la section 2.2 du document RFC 3986 comme réservés pour être potentiellement utilisés comme délimiteurs. Ceci est intentionnel et permet d’optimiser au maximum le jeu de caractères que l’argument de commande de l’URI peut prendre en charge sans avoir à coder ces caractères en pourcentage. 

  
Dans les segments < *command-argument* >, les caractères réservés dans le document RFC 3986 « : » et « / » font partie des données d’argument mais ne sont pas des délimiteurs, et sont donc inclus sans séquence d’échappement. 
  
### <a name="d-7-security-considerations"></a>D-7. Considérations relatives à la sécurité

Sur les systèmes qui ont enregistré des gestionnaires pour reconnaître et effectuer les actions des URI ms-visio, le fait de cliquer sur un lien vers un URI ms-visio entraîne le lancement de l’application enregistrée, avec des instructions pour que l’application tente d’ouvrir un document situé à l’URI spécifié. Les applications enregistrées pour traiter des URI ms-visio doivent mettre en œuvre des protections pour empêcher l’ouverture de documents provenant de systèmes distants non approuvés pouvant inclure du code malveillant.

  
### <a name="d-8-references"></a>D-8. Références

RFC 3987 – International Resource Identifiers (IRIs)
  
## <a name="appendix-e---uri-scheme-registration-template-for-ms-access-scheme"></a>ANNEXE E – MODÈLE D’ENREGISTREMENT DES MODÈLES D’URI POUR LE MODÈLE MS-ACCESS
<a name="bk_addresources"> </a>

### <a name="e-3-uri-scheme-syntax"></a>E-3. Syntaxe du modèle d’URI

> Modèle pour Access = "ms-access:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
    
> open-for-edit-cmd = "ofe|u|" document-uri
    
> open-for-view-cmd = "ofv|u|" document-uri
    
> new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]
    
> document-uri = URI d’emplacement du document à ouvrir
    
> template-uri = URI d’emplacement du modèle de fichier sur lequel le nouveau fichier sera basé
    
> save-location\* = URI d’emplacement du dossier dans lequel le nouveau document doit être créé
    
> \*save-location est un paramètre facultatif.
    
### <a name="e-4-uri-scheme-semantics"></a>E-4. Sémantique du modèle d’URI

Le modèle ms-access définit une syntaxe d’URI pour l’ouverture ou la création d’une base de données. Le modèle définit trois commandes qui font office d’instructions concernant les actions à effectuer avec le fichier de base de données. Les commandes sont 1) commande-ouvrir-pour-édition (ofe), qui donne l’instruction à l’application de base de données d’ouvrir la base de données située à l’URI spécifié pour édition ; 2) commande-ouvrir-pour-affichage (ofv), qui donne l’instruction à l’application de base de données d’ouvrir la base de données située à l’URI spécifié en mode lecture seule ; et 3) commande-créer-à-partir-d’un-modèle (nft), qui donne l’instruction à l’application de base de données de créer une base de données basée sur le modèle prédéfini situé à l’URI uri-du-modèle spécifié et d’enregistrer la nouvelle base de données dans l’emplacement spécifié dans l’URI emplacement-d’enregistrement facultatif ou, si cet URI facultatif n’a pas été spécifié, à l’emplacement de la bibliothèque de documents par défaut.
  
### <a name="e-5-applicationsprotocols-that-use-the-ms-access-uri-scheme"></a>E-5. Applications/Protocoles qui utilisent le modèle d’URI ms-access

Le modèle d’URI ms-access est utilisé par Microsoft Office 2013 pour appeler Microsoft Access 2013 ou Microsoft Access 2010 avec le Service Pack 2 à partir de pages web. Microsoft SharePoint 2013 utilise les URI ms-access comme des liens vers des bases de données Access stockées dans des bibliothèques de documents SharePoint.

  
### <a name="e-6-interoperability-considerations"></a>E-6. Considérations relatives à l’interopérabilité

Notez que la barre verticale utilisée comme délimiteur dans cette spécification ne fait pas partie des caractères identifiés à la section 2.2 du RFC 3986 qui sont réservés à un usage éventuel comme délimiteurs. Cette opération vise à optimiser le jeu de caractères que l’argument de commande de l’URI peut prendre en charge sans avoir à coder ces caractères en pourcentage. Dans les segments, les caractères réservés \<command-argument\> RFC 3986 « : » et « / » font partie des données d’argument, et non des délimiteur, et sont donc inclus sans séquence d’paysage.
  
### <a name="e-7-security-considerations"></a>E-7. Considérations relatives à la sécurité

Sur les systèmes qui ont enregistré des gestionnaires pour reconnaître et effectuer les actions des URI ms-access, le fait de cliquer sur un lien vers un URI ms-access entraîne le lancement de l’application enregistrée, avec des instructions pour que l’application tente d’ouvrir une base de données située à l’URI spécifié. Les applications enregistrées pour traiter des URI ms-access doivent mettre en œuvre des protections pour empêcher l’ouverture de bases de données provenant de systèmes distants non approuvés pouvant inclure du code malveillant.

  
### <a name="e-8-references"></a>E-8. Références

RFC 3987 – International Resource Identifiers (IRIs)  
  
## <a name="appendix-f---uri-scheme-registration-template-for-ms-project-scheme"></a>ANNEXE F – MODÈLE D’ENREGISTREMENT DES MODÈLES D’URI POUR LE MODÈLE MS-PROJECT
<a name="bk_addresources"> </a>

### <a name="f-3-uri-scheme-syntax"></a>F-3. Syntaxe du modèle d’URI

> Modèle pour Project = "ms-project:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
    
> open-for-edit-cmd = "ofe|u|" document-uri
    
> open-for-view-cmd = "ofv|u|" document-uri
    
> new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]
    
> document-uri = URI d’emplacement du document à ouvrir
    
> template-uri = URI d’emplacement du modèle de fichier sur lequel le nouveau fichier sera basé
    
> save-location\* = URI d’emplacement du dossier dans lequel le nouveau document doit être créé
    
> \*save-location est un paramètre facultatif.
    
### <a name="f-4-uri-scheme-semantics"></a>F-4. Sémantique du modèle d’URI

Le modèle ms-project définit une syntaxe d’URI pour l’ouverture ou la création d’un document Microsoft Project. Le modèle définit trois commandes qui font office d’instructions concernant les actions à effectuer avec le document référencé. Les commandes sont 1) commande-ouvrir-pour-édition (ofe), qui donne l’instruction à Project d’ouvrir le document situé à l’URI spécifié pour édition ; 2) commande-ouvrir-pour-affichage (ofv), qui donne l’instruction à Project d’ouvrir le document situé à l’URI spécifié en mode lecture seule ; et 3) commande-créer-à-partir-d’un-modèle (nft), qui donne l’instruction à Project de créer un document basé sur le modèle prédéfini de document situé à l’URI uri-du-modèle spécifié et d’enregistrer le nouveau document dans l’emplacement spécifié dans l’URI emplacement-d’enregistrement facultatif ou, si cet URI facultatif n’a pas été spécifié, à l’emplacement de la bibliothèque de documents par défaut.

  
### <a name="f-5-applicationsprotocols-that-use-the-ms-project-uri-scheme"></a>F-5. Applications/Protocoles qui utilisent le modèle d’URI ms-project

Le modèle d’URI ms-project est utilisé par Microsoft Office 2013 pour appeler Microsoft Project 2013 à partir de pages web. Microsoft SharePoint 2013 utilise les URI ms-project comme des liens vers des documents Project stockés dans des bibliothèques de documents SharePoint.

  
### <a name="f-6-interoperability-considerations"></a>F-6. Considérations relatives à l’interopérabilité

La barre verticale utilisée comme délimiteur dans cette spécification ne fait pas partie des caractères identifiés à la section 2.2 du document RFC 3986 comme réservés pour être potentiellement utilisés comme délimiteurs. Ceci est intentionnel et permet d’optimiser au maximum le jeu de caractères que l’argument de commande de l’URI peut prendre en charge sans avoir à coder ces caractères en pourcentage. 

  
Dans les segments < *command-argument* >, les caractères réservés dans le document RFC 3986 « : » et « / » font partie des données d’argument mais ne sont pas des délimiteurs, et sont donc inclus sans séquence d’échappement. 
  
### <a name="f-7-security-considerations"></a>F-7. Considérations relatives à la sécurité

Sur les systèmes qui ont enregistré des gestionnaires pour reconnaître et effectuer les actions des URI ms-project, le fait de cliquer sur un lien vers un URI ms-project entraîne le lancement de l’application enregistrée, avec des instructions pour que l’application tente d’ouvrir un document situé à l’URI spécifié. Les applications enregistrées pour traiter des URI ms-project doivent mettre en œuvre des protections pour empêcher l’ouverture de documents provenant de systèmes distants non approuvés pouvant inclure du code malveillant.

  
### <a name="f-8-references"></a>F-8. Références

RFC 3987 – International Resource Identifiers (IRIs)  
  
## <a name="appendix-g---uri-scheme-registration-template-for-ms-publisher-scheme"></a>ANNEXE G – MODÈLE D’ENREGISTREMENT DES MODÈLES D’URI POUR LE MODÈLE MS-PUBLISHER
<a name="bk_addresources"> </a>

### <a name="g-3-uri-scheme"></a>G-3. Modèle d’URI

> Modèle pour Publisher = "ms-publisher:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
    
> open-for-edit-cmd = "ofe|u|" document-uri
    
> open-for-view-cmd = "ofv|u|" document-uri
    
> new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]
    
> document-uri = URI d’emplacement du document à ouvrir
    
> template-uri = URI d’emplacement du modèle de fichier sur lequel le nouveau fichier sera basé
    
> save-location\* = URI d’emplacement du dossier dans lequel le nouveau document doit être créé
    
> \*save-location est un paramètre facultatif.
    
### <a name="g-4-uri-scheme-semantics"></a>G-4. Sémantique du modèle d’URI

Le modèle ms-publisher définit une syntaxe d’URI pour l’ouverture ou la création d’un document Microsoft Publisher. Le modèle définit trois commandes qui font office d’instructions concernant les actions à effectuer avec le document référencé. Les commandes sont 1) commande-ouvrir-pour-édition (ofe), qui donne l’instruction à Publisher d’ouvrir le document situé à l’URI spécifié pour édition ; 2) commande-ouvrir-pour-affichage (ofv), qui donne l’instruction à Publisher d’ouvrir le document situé à l’URI spécifié en mode lecture seule ; et 3) commande-créer-à-partir-d’un-modèle (nft), qui donne l’instruction à Publisher de créer un document basé sur le modèle prédéfini de document situé à l’URI uri-du-modèle spécifié et d’enregistrer le nouveau document dans l’emplacement spécifié dans l’URI emplacement-d’enregistrement facultatif ou, si cet URI facultatif n’a pas été spécifié, à l’emplacement de la bibliothèque de documents par défaut.
  
### <a name="g-5-applicationsprotocols-that-use-the-ms-publisher-uri-scheme"></a>G-5. Applications/Protocoles qui utilisent le modèle d’URI ms-publisher

Le modèle d’URI ms-publisher est utilisé par Microsoft Office 2013 pour appeler Microsoft Publisher 2013 ou Microsoft Publisher 2010 avec le Service Pack 2 à partir de pages web. Microsoft SharePoint 2013 utilise les URI ms-publisher comme des liens vers des documents Publisher stockés dans des bibliothèques de documents SharePoint.

  
### <a name="g-6-interoperability-considerations"></a>G-6. Considérations relatives à l’interopérabilité

Notez que la barre verticale utilisée comme délimiteur dans cette spécification ne fait pas partie des caractères identifiés à la section 2.2 du RFC 3986 qui sont réservés à un usage éventuel comme délimiteurs. Cette opération vise à optimiser le jeu de caractères que l’argument de commande de l’URI peut prendre en charge sans avoir à coder ces caractères en pourcentage. Dans les segments, les caractères réservés \<command-argument\> RFC 3986 « : » et « / » font partie des données d’argument, et non des délimiteur, et sont donc inclus sans séquence d’paysage.
  
### <a name="g-7-security-considerations"></a>G-7. Considérations relatives à la sécurité

Sur les systèmes qui ont enregistré des gestionnaires pour reconnaître et effectuer les actions des URI ms-publisher, le fait de cliquer sur un lien vers un URI ms-publisher entraîne le lancement de l’application enregistrée, avec des instructions pour que l’application tente d’ouvrir un document situé à l’URI spécifié. Les applications enregistrées pour traiter des URI ms-publisher doivent mettre en œuvre des protections pour empêcher l’ouverture de documents provenant de systèmes distants non approuvés pouvant inclure du code malveillant.
  
### <a name="g-9-references"></a>G-9. Références

RFC 3987 – International Resource Identifiers (IRIs)  
  
## <a name="appendix-h---uri-scheme-registration-template-for-ms-spd-scheme"></a>ANNEXE H – MODÈLE D’ENREGISTREMENT DES MODÈLES D’URI POUR LE MODÈLE MS-SPD
<a name="bk_addresources"> </a>

### <a name="h-3-uri-scheme-syntax"></a>H-3. Syntaxe du modèle d’URI

> Modèle pour SharePoint Designer = "ms-spd:" open-for-edit-cmd
    
> open-for-edit-cmd = "ofe|u|" document-uri
    
> document-uri = URI d’emplacement du document à ouvrir
    
### <a name="h-4-uri-scheme-semantics"></a>H-4. Sémantique du modèle d’URI

Le modèle ms-spd définit une syntaxe d’URI pour l’ouverture d’un document Microsoft SharePoint Designer. Le modèle définit deux commandes qui font office d’instructions concernant les actions à effectuer avec le document référencé. Les commandes sont 1) commande-ouvrir-pour-édition (ofe), qui donne l’instruction à SharePoint Designer d’ouvrir le document situé à l’URI spécifié pour édition ; 2) commande-ouvrir-pour-affichage (ofv), qui donne l’instruction à SharePoint Designer d’ouvrir le document situé à l’URI spécifié en mode lecture seule

  
### <a name="h-5-applicationsprotocols-that-use-the-ms-spd-uri-scheme"></a>H-5. Applications/Protocoles qui utilisent le modèle d’URI ms-spd

Le modèle d’URI ms-spd est utilisé par Microsoft Office 2013 pour appeler Microsoft SharePoint Designer 2013 à partir de pages web. Microsoft SharePoint 2013 utilise les URI ms-spd comme des liens vers des documents SharePoint Designer stockés dans des bibliothèques de documents SharePoint.

  
### <a name="h-6-interoperability-considerations"></a>H-6. Considérations relatives à l’interopérabilité

La barre verticale utilisée comme délimiteur dans cette spécification ne fait pas partie des caractères identifiés à la section 2.2 du document RFC 3986 comme réservés pour être potentiellement utilisés comme délimiteurs. Ceci est intentionnel et permet d’optimiser au maximum le jeu de caractères que l’argument de commande de l’URI peut prendre en charge sans avoir à coder ces caractères en pourcentage. 

  
Dans les segments < *command-argument* >, les caractères réservés dans le document RFC 3986 « : » et « / » font partie des données d’argument mais ne sont pas des délimiteurs, et sont donc inclus sans séquence d’échappement. 
  
### <a name="h-7-security-considerations"></a>H-7. Considérations relatives à la sécurité

Sur les systèmes qui ont enregistré des gestionnaires pour reconnaître et effectuer les actions des URI ms-spd, le fait de cliquer sur un lien vers un URI ms-spd entraîne le lancement de l’application enregistrée, avec des instructions pour que l’application tente d’ouvrir un document situé à l’URI spécifié. Les applications enregistrées pour traiter des URI ms-spd doivent mettre en œuvre des protections pour empêcher l’ouverture de documents provenant de systèmes distants non approuvés pouvant inclure du code malveillant.

  
### <a name="h-8-references"></a>H-8. Références

RFC 3987 – International Resource Identifiers (IRIs)  
  
## <a name="appendix-i---uri-scheme-registration-template-for-ms-infopath-scheme"></a>ANNEXE I – MODÈLE D’ENREGISTREMENT DES MODÈLES D’URI POUR LE MODÈLE MS-INFOPATH
<a name="bk_addresources"> </a>

###   <a name="i-3-uri-scheme-syntax"></a>I-3. Syntaxe du modèle d’URI

> Modèle pour Infopath = "ms-infopath:" open-for-edit-cmd | open-for-view-cmd
    
> open-for-edit-cmd = "ofe|u|" document-uri
    
> open-for-view-cmd = "ofv|u|" document-uri
    
> document-uri = URI d’emplacement du document à ouvrir
    
### <a name="i-4-uri-scheme-semantics"></a>I-4. Sémantique du modèle d’URI

Le modèle ms-infopath définit une syntaxe d’URI pour l’ouverture ou la création d’un document Microsoft Infopath. Le modèle définit deux commandes qui font office d’instructions concernant les actions à effectuer avec le document référencé. Les commandes sont 1) open-for-edit-cmd (ofe), ce qui indique à InfoPath d’ouvrir le document à l’URI spécifié pour modification ; et 2) commande-ouvrir-pour-affichage (ofv), qui demande à InfoPath d’ouvrir le document à l’URI spécifié en mode lecture seule.
  
### <a name="i-5-applicationsprotocols-that-use-the-ms-infopath-uri-scheme"></a>I-5. Applications/Protocoles qui utilisent le modèle d’URI ms-infopath

Le modèle d’URI ms-infopath est utilisé par Microsoft Office 2013 pour appeler Microsoft Infopath 2013 à partir de pages web. Microsoft SharePoint 2013 utilise les URI ms-infopath comme des liens vers des documents Infopath stockés dans des bibliothèques de documents SharePoint.
  
### <a name="i-6-interoperability-considerations"></a>I-6. Considérations relatives à l’interopérabilité

La barre verticale utilisée comme délimiteur dans cette spécification ne fait pas partie des caractères identifiés à la section 2.2 du document RFC 3986 comme réservés pour être potentiellement utilisés comme délimiteurs. Ceci est intentionnel et permet d’optimiser au maximum le jeu de caractères que l’argument de commande de l’URI peut prendre en charge sans avoir à coder ces caractères en pourcentage. 

  
Dans les segments < *command-argument* >, les caractères réservés dans le document RFC 3986 « : » et « / » font partie des données d’argument mais ne sont pas des délimiteurs, et sont donc inclus sans séquence d’échappement. 
  
### <a name="i-7-security-considerations"></a>I-7. Considérations relatives à la sécurité

Sur les systèmes qui ont enregistré des gestionnaires pour reconnaître et effectuer les actions des URI ms-infopath, le fait de cliquer sur un lien vers un URI ms-infopath entraîne le lancement de l’application enregistrée, avec des instructions pour que l’application tente d’ouvrir un document situé à l’URI spécifié. Les applications enregistrées pour traiter des URI ms-infopath doivent mettre en œuvre des protections pour empêcher l’ouverture de documents provenant de systèmes distants non approuvés pouvant inclure du code malveillant.

  
### <a name="i-8-references"></a>I-8. Références

RFC 3987 – International Resource Identifiers (IRIs)  
  
