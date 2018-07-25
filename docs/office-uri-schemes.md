---
title: Modèles d’URI Office
manager: luken
ms.date: 01/14/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1ea99a8f-b005-4b92-b313-923294d20fbf
ms.openlocfilehash: 834c4d2c2f47c6cc3f35423a7dfe3c13caf3d209
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782523"
---
# <a name="office-uri-schemes"></a><span data-ttu-id="db336-102">Modèles d’URI Office</span><span class="sxs-lookup"><span data-stu-id="db336-102">Office URI Schemes</span></span>

## <a name="11-abstract"></a><span data-ttu-id="db336-103">1.1 RÉSUMÉ</span><span class="sxs-lookup"><span data-stu-id="db336-103">1.1	ABSTRACT</span></span>

<span data-ttu-id="db336-104">Ce document définit le format des URI (Uniform Resource Identifier) pour les applications de productivité Office.</span><span class="sxs-lookup"><span data-stu-id="db336-104">This document defines the format of Uniform Resource Identifiers (URIs) for office productivity applications.</span></span> <span data-ttu-id="db336-105">Ce modèle est pris en charge dans Microsoft Office 2010 Service Pack 2 et versions ultérieures, y compris Microsoft Office 2013 pour Windows et les produits Microsoft SharePoint 2013.</span><span class="sxs-lookup"><span data-stu-id="db336-105">This document defines the format of Uniform Resource Identifiers (URIs) for office productivity applications. The scheme is supported in Microsoft Office 2010 Service Pack 2 and later, including the Microsoft Office 2013 for Windows and the Microsoft SharePoint 2013 products.
It is also supported in Office for iPhone, Office for iPad, and Office for Mac 2011.</span></span> <span data-ttu-id="db336-106">Il est également pris en charge dans Office pour iPhone, Office pour iPad et Microsoft Office pour Mac 2011.</span><span class="sxs-lookup"><span data-stu-id="db336-106">It is also supported in Office for iPhone, Office for iPad, and Office for Mac 2011.</span></span>
  
## <a name="12-introduction"></a><span data-ttu-id="db336-107">1.2 INTRODUCTION</span><span class="sxs-lookup"><span data-stu-id="db336-107">1.2	INTRODUCTION</span></span>

<span data-ttu-id="db336-108">Ces modèles d’URI permettent d’appeler les applications de productivité Office à l’aide de différentes commandes.</span><span class="sxs-lookup"><span data-stu-id="db336-108">These URI schemes allow for office productivity applications to be invoked with various commands.</span></span> <span data-ttu-id="db336-109">À chaque application correspond un modèle, mais tous les modèles respectent les mêmes règles de mise en forme de l’URI (modèle d’URI).</span><span class="sxs-lookup"><span data-stu-id="db336-109">These URI schemes allow for office productivity applications to be invoked with various commands. Each application is given a different named scheme but all schemes follow the same rules for how the URI is formed (URI Schema).
</span></span>
  
## <a name="13-uri-schema"></a><span data-ttu-id="db336-110">1.3 MODÈLE D’URI</span><span class="sxs-lookup"><span data-stu-id="db336-110">1.3	URI SCHEMA</span></span>

### <a name="full-schema"></a><span data-ttu-id="db336-111">Modèle complet</span><span class="sxs-lookup"><span data-stu-id="db336-111">Full schema</span></span>

<span data-ttu-id="db336-112">< *scheme-name*  >:<  *command-name*  >"|"<  *command-argument-descriptor*  > "|"<  *command-argument*  ></span><span class="sxs-lookup"><span data-stu-id="db336-112">< *scheme-name*  >:<  *command-name*  >"|"<  *command-argument-descriptor*  > "|"<  *command-argument*  ></span></span> 
  
<span data-ttu-id="db336-113">Un URI, tel que défini dans ce document, peut comporter un ou plusieurs arguments de commande, qui peuvent chacun contenir les éléments < *command-argument-descriptor* > et < *command-argument* > et être délimités par une barre verticale (« | »).</span><span class="sxs-lookup"><span data-stu-id="db336-113">A URI as defined in this document may have one or more command arguments, each of which must include both the < *command-argument-descriptor*  > and the <  *command-argument*  > elements and be delimited by the vertical bar ("|") character.</span></span> <span data-ttu-id="db336-114">Quand l’URI comporte plusieurs arguments de commande, une barre verticale (« | ») doit délimiter chaque argument de commande de l’argument suivant.</span><span class="sxs-lookup"><span data-stu-id="db336-114">When more than one command argument is included in a URI there must be a vertical bar ("|") character separating each command argument from the following command argument.</span></span> 
  
<span data-ttu-id="db336-115">Ces modèles ne contiennent pas de composant d’autorité comme défini dans la section 3.2 du RFC 3986.</span><span class="sxs-lookup"><span data-stu-id="db336-115">These schemes do not include an authority component as defined in section 3.2 of RFC 3986.</span></span> <span data-ttu-id="db336-116">Les commandes spécifiées dans ce document sont appelées quand le système appelle la commande.</span><span class="sxs-lookup"><span data-stu-id="db336-116">Invocation of the commands specified in this document takes place in the context of the system invoking the command.</span></span> <span data-ttu-id="db336-117">Par exemple, quand l’URI « ms-excel:ofv|u|http://contoso/Q4/budget.xls » est appelé à partir d’un ordinateur personnel exécutant Microsoft Windows doté de Microsoft Office 2013, l’application locale Microsoft Excel est généralement lancée et transmet les arguments pour ouvrir ce fichier dans  *http://contoso/Q4/budget.xls*  en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="db336-117">For example, when the URI "ms-excel:ofv|u|http://contoso/Q4/budget.xls" is invoked from a personal computer running Microsoft Windows with Microsoft Office 2013 installed the expected result is that the local installation of Microsoft Excel will be launched and passed arguments to open the file at  *http://contoso/Q4/budget.xls*  in read-only mode.</span></span> <span data-ttu-id="db336-118">Notez que la barre verticale utilisée comme délimiteur dans cette spécification ne fait pas partie des caractères identifiés à la section 2.2 du RFC 3986 qui sont réservés à un usage éventuel comme délimiteurs.</span><span class="sxs-lookup"><span data-stu-id="db336-118">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters. 
</span></span> <span data-ttu-id="db336-119">Cette opération vise à optimiser le jeu de caractères que l’argument de commande de l’URI peut prendre en charge sans avoir à coder ces caractères en pourcentage.</span><span class="sxs-lookup"><span data-stu-id="db336-119">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters. 
</span></span> 
  
<span data-ttu-id="db336-120">La syntaxe du modèle inclut les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="db336-120">The scheme syntax includes the following:</span></span>
  
1. <span data-ttu-id="db336-121">< *scheme-name*  > : type de l’application à appeler.</span><span class="sxs-lookup"><span data-stu-id="db336-121">< *scheme-name*  >: This refers to the type of application that should be invoked.</span></span> <span data-ttu-id="db336-122">Par exemple, le nom de modèle ms-word: est déposé par Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="db336-122"><scheme-name>: This refers to the type of application that should be invoked. For instance, the ms-word: scheme name is registered by Microsoft Word.
</span></span> 
    
2. <span data-ttu-id="db336-123">Délimiteur « : »</span><span class="sxs-lookup"><span data-stu-id="db336-123">“:” separator
</span></span>
    
3. <span data-ttu-id="db336-124">< *command-name*  > : décrit les actions que l’application doit effectuer.</span><span class="sxs-lookup"><span data-stu-id="db336-124">< *command-name*  >: This describes the actions that the application should perform.</span></span> <span data-ttu-id="db336-125">Par exemple, ouvrir un document pour le consulter.</span><span class="sxs-lookup"><span data-stu-id="db336-125">For instance, opening a document for viewing.</span></span> <span data-ttu-id="db336-126">La liste des noms de commande figure à la section 1.5.</span><span class="sxs-lookup"><span data-stu-id="db336-126">The list of command names is described in section 1.5.</span></span> 
    
4. <span data-ttu-id="db336-127">Délimiteur « | » (barre verticale)</span><span class="sxs-lookup"><span data-stu-id="db336-127">“|” (vertical bar) separator
</span></span>
    
5. <span data-ttu-id="db336-128">< *command-argument-descriptor*  > : cet élément fournit davantage d’informations sur l’objet de l’argument de commande.</span><span class="sxs-lookup"><span data-stu-id="db336-128"><command-argument-descriptor>: This element gives more information about what the command argument is about. 
</span></span> 
    
6. <span data-ttu-id="db336-129">Délimiteur « | » (barre verticale)</span><span class="sxs-lookup"><span data-stu-id="db336-129">“|” (vertical bar) separator
</span></span>
    
7. <span data-ttu-id="db336-130">< *command-argument*  > : les arguments varient en fonction de la commande.</span><span class="sxs-lookup"><span data-stu-id="db336-130">< *command-argument*  >: The arguments vary depending on the command.</span></span> <span data-ttu-id="db336-131">L’URI vers un document est un argument courant qui utilise généralement le modèle http ou https.</span><span class="sxs-lookup"><span data-stu-id="db336-131">One common argument is the URI to a document, typically using the http or https scheme.</span></span> <span data-ttu-id="db336-132">Notez que, dans les segments <  *command-argument*  >, les caractères réservés dans le document RFC 3986 « : » et « / » font partie des données d’argument mais ne sont pas des délimiteurs, et sont donc inclus sans séquence d’échappement.</span><span class="sxs-lookup"><span data-stu-id="db336-132">Note that within <  *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
    
### <a name="abbreviated-schema"></a><span data-ttu-id="db336-133">Modèle abrégé</span><span class="sxs-lookup"><span data-stu-id="db336-133">Abbreviated schema</span></span>

<span data-ttu-id="db336-134">Une forme abrégée des modèles d’URI Office permet à une demande plus compacte de lancer une application Office spécifiée pour ouvrir la ressource située à un URI donné.</span><span class="sxs-lookup"><span data-stu-id="db336-134">
An abbreviated  form of the office URI schemes allows for a more compact request to launch a specified Office application to open the resource located at a given URI. This abbreviated form implies the <command-name> “ofv” and the <command-argument-descriptor> “u”. No further commands or command arguments are allowed in this schema.</span></span> <span data-ttu-id="db336-135">Cette forme abrégée indique les éléments < < *command-name*  > "ofv" et <  *command-argument-descriptor*  > "u".</span><span class="sxs-lookup"><span data-stu-id="db336-135">This abbreviated form implies the < *command-name*  > "ofv" and the <  *command-argument-descriptor*  > "u".</span></span> <span data-ttu-id="db336-136">Aucune commande, ni aucun argument de commande, n’est autorisé dans ce schéma.</span><span class="sxs-lookup"><span data-stu-id="db336-136">No further commands or command arguments are allowed in this schema.</span></span> 
  
<span data-ttu-id="db336-137">< *scheme-name*  >:<  *command-argument*  ></span><span class="sxs-lookup"><span data-stu-id="db336-137">< *scheme-name*  >:<  *command-argument*  ></span></span> 
  
1. <span data-ttu-id="db336-138">< *scheme-name*  > : type de l’application à appeler.</span><span class="sxs-lookup"><span data-stu-id="db336-138">< *scheme-name*  >: the type of application that should be invoked.</span></span> <span data-ttu-id="db336-139">Par exemple, ms-word: pour Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="db336-139">For instance ms-word: for Microsoft Word.</span></span> 
    
2. <span data-ttu-id="db336-140">< *command-argument*  > : URI de la ressource que l’application doit ouvrir.</span><span class="sxs-lookup"><span data-stu-id="db336-140">< *command-argument*  >: URI for the resource the application should open.</span></span> <span data-ttu-id="db336-141">Actuellement, seuls les URI basés sur le modèle http ou https sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="db336-141"><command-argument>:  URI for the resource the application should open. Currently only URIs based on the http or https scheme are supported.
</span></span> 
    
## <a name="14-scheme-names-and-office-application-registrations"></a><span data-ttu-id="db336-142">1.4 NOM DES MODÈLES ET ENREGISTREMENT DES APPLICATIONS OFFICE</span><span class="sxs-lookup"><span data-stu-id="db336-142">1.4	SCHEME NAMES AND OFFICE APPLICATION REGISTRATIONS</span></span>

<span data-ttu-id="db336-143">Voici la liste des noms de modèles implémentés dans les applications Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="db336-143">The following is the list of scheme names implemented in Microsoft Office applications.</span></span> <span data-ttu-id="db336-144">Quand Microsoft Office est installé, chaque nom de modèle est enregistré dans Windows pour être géré par le produit Office du même nom.</span><span class="sxs-lookup"><span data-stu-id="db336-144">
The following is the list of scheme names implemented in Microsoft Office applications. When Microsoft Office is installed, each scheme name is registered with Windows to be handled by the Office product of the same name. Note that “ms-spd” is an abbreviation for SharePoint Designer.</span></span> <span data-ttu-id="db336-145">Notez que « ms-spd » est une abréviation de SharePoint Designer.</span><span class="sxs-lookup"><span data-stu-id="db336-145">Note that "ms-spd" is an abbreviation for SharePoint Designer.</span></span>
  
> - <span data-ttu-id="db336-146">*ms-word:*</span><span class="sxs-lookup"><span data-stu-id="db336-146">*ms-word:*</span></span> 
    
> - <span data-ttu-id="db336-147">*ms-powerpoint:*</span><span class="sxs-lookup"><span data-stu-id="db336-147">*ms-powerpoint:*</span></span> 
    
> - <span data-ttu-id="db336-148">*ms-excel:*</span><span class="sxs-lookup"><span data-stu-id="db336-148">*ms-excel:*</span></span> 
    
> - <span data-ttu-id="db336-149">*ms-visio:*</span><span class="sxs-lookup"><span data-stu-id="db336-149">-	*ms-visio:*</span></span> 
    
> - <span data-ttu-id="db336-150">*ms-access:*</span><span class="sxs-lookup"><span data-stu-id="db336-150">*ms-access:*</span></span> 
    
> - <span data-ttu-id="db336-151">*ms-project:*</span><span class="sxs-lookup"><span data-stu-id="db336-151">*ms-project:*</span></span> 
    
> - <span data-ttu-id="db336-152">*ms-publisher:*</span><span class="sxs-lookup"><span data-stu-id="db336-152">-	*ms-publisher: 
*</span></span> 
    
> - <span data-ttu-id="db336-153">*ms-spd:*</span><span class="sxs-lookup"><span data-stu-id="db336-153">-	*ms-spd:
*</span></span> 
    
> - <span data-ttu-id="db336-154">*ms-infopath:*</span><span class="sxs-lookup"><span data-stu-id="db336-154">-	*ms-infopath:*</span></span> 
    
## <a name="15-commands-and-required-command-arguments"></a><span data-ttu-id="db336-155">1.5 COMMANDES ET ARGUMENTS DE COMMANDE REQUIS</span><span class="sxs-lookup"><span data-stu-id="db336-155">1.5	COMMANDS AND REQUIRED COMMAND ARGUMENTS
</span></span>

### <a name="view-document"></a><span data-ttu-id="db336-156">Afficher le document</span><span class="sxs-lookup"><span data-stu-id="db336-156">View Document</span></span>

<span data-ttu-id="db336-157">La commande suivante force l’application à ouvrir le document référencé par l’URI en mode Lecture seule ou Affichage.</span><span class="sxs-lookup"><span data-stu-id="db336-157">The following command will cause the application to open the document referenced by the URI in a read-only or view mode.</span></span>
  
> <span data-ttu-id="db336-158">Nom de la commande : ofv</span><span class="sxs-lookup"><span data-stu-id="db336-158">Command Name: ofv</span></span>
    
> <span data-ttu-id="db336-159">Descripteur de l’argument de commande : u</span><span class="sxs-lookup"><span data-stu-id="db336-159">Command argument descriptor: u</span></span>
    
> <span data-ttu-id="db336-160">Argument de commande : URI vers le document, construit sur le modèle http ou https</span><span class="sxs-lookup"><span data-stu-id="db336-160">Command argument: a URI to the document, based on the http or https scheme</span></span>
    
> <span data-ttu-id="db336-161">Exemple : *ms-excel:ofv|u|http://contoso/Q4/budget.xls*</span><span class="sxs-lookup"><span data-stu-id="db336-161">Example:  *ms-excel:ofv|u|http://contoso/Q4/budget.xls*</span></span> 
    
### <a name="edit-document"></a><span data-ttu-id="db336-162">Modifier le document</span><span class="sxs-lookup"><span data-stu-id="db336-162">Edit Document</span></span>

<span data-ttu-id="db336-163">La commande suivante force l’application à ouvrir le document référencé par l’URI en mode Édition.</span><span class="sxs-lookup"><span data-stu-id="db336-163">The following command will cause the application to open the document referenced by the URI in editing mode.</span></span>
  
> <span data-ttu-id="db336-164">Nom de la commande : ofe</span><span class="sxs-lookup"><span data-stu-id="db336-164">Command Name: ofe</span></span>
    
> <span data-ttu-id="db336-165">Descripteur de l’argument de commande : u</span><span class="sxs-lookup"><span data-stu-id="db336-165">Command argument descriptor: u</span></span>
    
> <span data-ttu-id="db336-166">Argument de commande : URI vers le document, construit sur le modèle http ou https</span><span class="sxs-lookup"><span data-stu-id="db336-166">Command argument: a URI to the document, based on the http or https scheme</span></span>
    
> <span data-ttu-id="db336-167">Exemple :  *ms-powerpoint:ofe|u|http://www.fourthcoffee.com/AllHandsDeck.ppt*</span><span class="sxs-lookup"><span data-stu-id="db336-167">Example:  *ms-powerpoint:ofe|u|http://www.fourthcoffee.com/AllHandsDeck.ppt*</span></span> 
    
### <a name="new-document-from-template"></a><span data-ttu-id="db336-168">Nouveau document à partir d’un modèle</span><span class="sxs-lookup"><span data-stu-id="db336-168">New Document from Template</span></span>

<span data-ttu-id="db336-169">La commande suivante force l’application à créer et à ouvrir un nouveau document basé sur le modèle stocké à l’URI spécifié.</span><span class="sxs-lookup"><span data-stu-id="db336-169">The following command will cause the application to create and open a new document based on the template stored at the specified URI.</span></span> <span data-ttu-id="db336-170">Le modèle de fichier n’est pas modifié au cours de ce processus.</span><span class="sxs-lookup"><span data-stu-id="db336-170">The template file is not modified in this process.</span></span> <span data-ttu-id="db336-171">Un argument de commande supplémentaire peut être renseigné pour spécifier le chemin d’accès par défaut proposé comme emplacement d’enregistrement, quand le fichier est enregistré pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="db336-171">An additional command argument may be supplied to specify the default path offered as a save location when the file is first saved.</span></span> <span data-ttu-id="db336-172">L’utilisateur peut alors choisir un autre emplacement.</span><span class="sxs-lookup"><span data-stu-id="db336-172">It is possible for the user to choose a different location.</span></span>
  
> <span data-ttu-id="db336-173">Nom de la commande : nft</span><span class="sxs-lookup"><span data-stu-id="db336-173">Command Name: nft</span></span>
    
> <span data-ttu-id="db336-174">Descripteur de l’argument de commande 1 : u</span><span class="sxs-lookup"><span data-stu-id="db336-174">Command argument descriptor 1: u</span></span>
    
> <span data-ttu-id="db336-175">Argument de commande 1 : URI vers le modèle, construit sur le modèle http ou https</span><span class="sxs-lookup"><span data-stu-id="db336-175">Command argument 1: a URI to the template, based on the http or https scheme</span></span>
    
> <span data-ttu-id="db336-176">Descripteur de l’argument de commande 2 : s</span><span class="sxs-lookup"><span data-stu-id="db336-176">Optional Command argument descriptor 2: s</span></span>
    
> <span data-ttu-id="db336-177">Argument de commande facultatif 2 : URI pour spécifier le dossier d’enregistrement par défaut</span><span class="sxs-lookup"><span data-stu-id="db336-177">Optional Command argument 2: URI to specify the default save folder</span></span>
    
> <span data-ttu-id="db336-178">Exemple :  *ms-word:nft|u|http://cohowinery/templates/elegance.pot|s|http://cohowinery/presentations*</span><span class="sxs-lookup"><span data-stu-id="db336-178">Example:  *ms-word:nft|u|http://cohowinery/templates/elegance.pot|s|http://cohowinery/presentations*</span></span> 
    
<span data-ttu-id="db336-179">Si l’emplacement d’enregistrement par défaut facultatif est renseigné, il doit pointer vers le même nom d’hôte que le modèle.</span><span class="sxs-lookup"><span data-stu-id="db336-179">As a note, if the optional default save location is supplied, it must be pointing to the same host name as the template.</span></span>
  
<span data-ttu-id="db336-180">De plus, les applications SharePoint Designer et InfoPath (qui implémentent les modèles ms-sdp: et ms-infopath:, respectivement) ne prennent pas en charge la fonctionnalité de création d’un nouveau document à partir d’un modèle.</span><span class="sxs-lookup"><span data-stu-id="db336-180">Additionally, the SharePoint Designer and InfoPath applications (which implement the ms-spd: scheme and ms-infopath: schemes, respectively) do not support the “new document from template” functionality.
</span></span>
  
## <a name="16-backwards-compatibility"></a><span data-ttu-id="db336-181">1.6 COMPATIBILITÉ DESCENDANTE</span><span class="sxs-lookup"><span data-stu-id="db336-181">1.6	BACKWARDS COMPATIBILITY</span></span>

<span data-ttu-id="db336-182">Quand le gestionnaire d’URI Office analyse l’URI pour extraire les arguments de commande correspondant à une commande spécifique, il utilise uniquement les arguments de commande ayant le descripteur d’argument de commande attendu.</span><span class="sxs-lookup"><span data-stu-id="db336-182">When parsing a URI to extract the appropriate command arguments for a given command, the Office URI handler will only use the command arguments that have the expected command argument descriptor.</span></span> <span data-ttu-id="db336-183">Si d’autres paires d’arguments et descripteurs d’argument contiennent des descripteurs d’argument inattendus, ils sont supprimés de l’URI.</span><span class="sxs-lookup"><span data-stu-id="db336-183">If there are additional pairs of arguments and argument descriptors that have unexpected argument descriptors, they will be removed from the URI.</span></span> <span data-ttu-id="db336-184">Ce mécanisme permet aux versions ultérieures du modèle d’ajouter d’autres arguments de commande sans compromettre la compatibilité descendante avec les implémentations héritées de ce modèle.</span><span class="sxs-lookup"><span data-stu-id="db336-184">This mechanism allows future versions of the scheme to add additional command arguments without breaking backward compatibility with legacy implementations of this scheme.</span></span>
  
## <a name="17-implementation-restrictions-on-command-arguments"></a><span data-ttu-id="db336-185">1.7 RESTRICTIONS D’IMPLÉMENTATION SUR LES ARGUMENTS DE COMMANDE</span><span class="sxs-lookup"><span data-stu-id="db336-185">1.7	IMPLEMENTATION RESTRICTIONS ON COMMAND ARGUMENTS</span></span>

<span data-ttu-id="db336-186">Les restrictions suivantes sont placées sur des arguments de commande dans leur implémentation actuelle dans Office 2013.</span><span class="sxs-lookup"><span data-stu-id="db336-186">The below restrictions are placed on command arguments in its current implementation in Office 2013.</span></span>
  
### <a name="length-limitations-on-uri-command-arguments"></a><span data-ttu-id="db336-187">Limitations de longueur des arguments de commande des URI</span><span class="sxs-lookup"><span data-stu-id="db336-187">Length limitations on URI command arguments</span></span>

<span data-ttu-id="db336-188">Le chemin d’accès des arguments de commande des URI ne doit pas comporter plus de 256 caractères pour toutes les applications sauf Excel (216 caractères max.).</span><span class="sxs-lookup"><span data-stu-id="db336-188">For URI command arguments, the maximum path length is 256 characters for all apps except Excel, where the limit is 216. Path lengths greater than these may be supported on an app-by-app basis and testing is recommended before deploying any solutions that rely on this.

</span></span> <span data-ttu-id="db336-189">Les chemins d’accès trop longs peuvent être pris en charge selon l’application. Nous vous recommandons de réaliser des tests avant de déployer des solutions qui dépendent de ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="db336-189">For URI command arguments, the maximum path length is 256 characters for all apps except Excel, where the limit is 216. Path lengths greater than these may be supported on an app-by-app basis and testing is recommended before deploying any solutions that rely on this.

</span></span>
  
### <a name="allowed-characters-in-uri-command-arguments"></a><span data-ttu-id="db336-190">Caractères autorisés dans les arguments de commande des URI</span><span class="sxs-lookup"><span data-stu-id="db336-190">Allowed characters in URI command arguments</span></span>

<span data-ttu-id="db336-191">Les URI autorisés doivent respecter les normes mentionnées dans le RFC 3987 – Internationalized Resource Identifiers (IRIs).</span><span class="sxs-lookup"><span data-stu-id="db336-191">Allowed URIs must conform to the standards proposed in RFC 3987 - Internationalized Resource Identifiers (IRIs) .</span></span> <span data-ttu-id="db336-192">Les caractères identifiés comme étant réservés dans le RFC 3986 ne doivent pas être codés en pourcentage.</span><span class="sxs-lookup"><span data-stu-id="db336-192">Characters identified as reserved in RFC 3986 should not be percent encoded.</span></span> <span data-ttu-id="db336-193">.</span><span class="sxs-lookup"><span data-stu-id="db336-193"></span></span> <span data-ttu-id="db336-194">Les noms de fichiers ne peuvent pas contenir les caractères suivants : \ / : ?</span><span class="sxs-lookup"><span data-stu-id="db336-194">Filenames must not contain any of the following characters: \ / : ?</span></span> <span data-ttu-id="db336-195">\< \> | " ou \*.</span><span class="sxs-lookup"><span data-stu-id="db336-195">\< \> | " or \*.</span></span>  
  
## <a name="appendix-a---uri-scheme-registration-template-for-ms-word-scheme"></a><span data-ttu-id="db336-196">ANNEXE A – MODÈLE D’ENREGISTREMENT DES MODÈLES D’URI POUR LE MODÈLE MS-WORD</span><span class="sxs-lookup"><span data-stu-id="db336-196">APPENDIX A – URI SCHEME REGISTRATION TEMPLATE FOR MS-WORD SCHEME
</span></span>
<span data-ttu-id="db336-197"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="db336-197"></span></span>

### <a name="a-3-uri-scheme-syntax"></a><span data-ttu-id="db336-198">A-3.</span><span class="sxs-lookup"><span data-stu-id="db336-198">A-3.</span></span> <span data-ttu-id="db336-199">Syntaxe du modèle d’URI</span><span class="sxs-lookup"><span data-stu-id="db336-199">E-3.	URI Scheme Syntax</span></span>

> <span data-ttu-id="db336-200">Modèle pour Word = "ms-word:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="db336-200">Word Scheme 	=	“ms-word:” open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
</span></span>
    
> <span data-ttu-id="db336-201">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="db336-201">open-for-edit-cmd	= “ofe|u|” document-uri
</span></span>
    
> <span data-ttu-id="db336-202">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="db336-202">open-for-view-cmd	= “ofv|u|” document-uri</span></span>
    
> <span data-ttu-id="db336-203">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="db336-203">new-from-template-cmd = “nft|u|” template-uri [“|s|” save-location]</span></span>
    
> <span data-ttu-id="db336-204">document-uri = URI d’emplacement du document à ouvrir</span><span class="sxs-lookup"><span data-stu-id="db336-204">
document-uri	=	URI location of document to open</span></span>
    
> <span data-ttu-id="db336-205">template-uri = URI d’emplacement du modèle de fichier sur lequel le nouveau fichier sera basé</span><span class="sxs-lookup"><span data-stu-id="db336-205">template-uri	=	URI location of template file upon which new file will be based
</span></span>
    
> <span data-ttu-id="db336-206">save-location = URI d’emplacement du dossier dans lequel le nouveau document doit être créé</span><span class="sxs-lookup"><span data-stu-id="db336-206">save-location\*	= URI location of folder in which new document should be created</span></span>
    
### <a name="a-4-uri-scheme-semantics"></a><span data-ttu-id="db336-207">A-4.</span><span class="sxs-lookup"><span data-stu-id="db336-207">A-4.</span></span> <span data-ttu-id="db336-208">Sémantique du modèle d’URI</span><span class="sxs-lookup"><span data-stu-id="db336-208">H-4.	URI Scheme Semantics
</span></span>

<span data-ttu-id="db336-209">Le modèle ms-word définit une syntaxe d’URI pour ouvrir et créer un document de traitement de texte.</span><span class="sxs-lookup"><span data-stu-id="db336-209">The ms-word scheme defines a URI syntax for opening or creating a word processing document.</span></span> <span data-ttu-id="db336-210">Le modèle définit trois commandes qui indiquent les actions à effectuer avec le document référencé.</span><span class="sxs-lookup"><span data-stu-id="db336-210">The scheme defines three commands that serve as instructions regarding what should be done with the referenced document.</span></span> <span data-ttu-id="db336-211">Les commandes sont 1) open-for-edit-cmd (ofe), qui demande à une application de traitement de texte d’ouvrir pour modification le document situé à l’URI spécifié ; 2) open-for-view-cmd (ofv), qui demande à une application de traitement de texte d’ouvrir en lecture seule le document situé à l’URI spécifié ; et 3) new-from-template-cmd (nft), qui demande à une application de traitement de texte de créer un document basé sur le modèle de document situé à l’URI template-uri spécifié et d’enregistrer le nouveau document à l’emplacement spécifié dans l’URI save-location facultatif ou, si cet URI facultatif n’a pas été spécifié, à l’emplacement de la bibliothèque de documents par défaut.</span><span class="sxs-lookup"><span data-stu-id="db336-211">The ms-word scheme defines a URI syntax for opening or creating a word processing document. The scheme defines three commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs a word processing application to open the document at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs a word processing application to open the document at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs a word processing application to create a new document based on the document template located at the specified template-uri URI and save the new document either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.
</span></span>
  
### <a name="a-5-applicationsprotocols-that-use-the-ms-word-uri-scheme"></a><span data-ttu-id="db336-212">A-5.</span><span class="sxs-lookup"><span data-stu-id="db336-212">A-5.</span></span> <span data-ttu-id="db336-213">Applications/Protocoles qui utilisent le modèle d’URI ms-word</span><span class="sxs-lookup"><span data-stu-id="db336-213">A-5.	Applications/Protocols that use the ms-word URI Scheme
</span></span>

<span data-ttu-id="db336-214">Microsoft Office 2013 utilise le modèle d’URI ms-word pour appeler Microsoft Word 2013 ou Microsoft Word 2010 avec Service Pack 2.</span><span class="sxs-lookup"><span data-stu-id="db336-214">The ms-word URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Word 2013 or Microsoft Word 2010 with Service Pack 2. Microsoft SharePoint 2013 uses ms-word URIs as links to word processing documents stored in SharePoint document libraries.
</span></span> <span data-ttu-id="db336-215">Microsoft SharePoint 2013 utilise les URI ms-word pour rediriger vers des documents de traitement de texte enregistrés dans les bibliothèques de documents SharePoint.</span><span class="sxs-lookup"><span data-stu-id="db336-215">The ms-word URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Word 2013 or Microsoft Word 2010 with Service Pack 2. Microsoft SharePoint 2013 uses ms-word URIs as links to word processing documents stored in SharePoint document libraries.
</span></span>
  
### <a name="a-6-interoperability-considerations"></a><span data-ttu-id="db336-216">A-6.</span><span class="sxs-lookup"><span data-stu-id="db336-216">A-6.</span></span> <span data-ttu-id="db336-217">Considérations relatives à l’interopérabilité</span><span class="sxs-lookup"><span data-stu-id="db336-217">
G-6.	Interoperability Considerations 
</span></span>

<span data-ttu-id="db336-218">Notez que la barre verticale utilisée comme délimiteur dans cette spécification ne fait pas partie des caractères identifiés à la section 2.2 du RFC 3986 qui sont réservés à un usage éventuel comme délimiteurs.</span><span class="sxs-lookup"><span data-stu-id="db336-218">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters. 
</span></span> <span data-ttu-id="db336-219">Cette opération vise à optimiser le jeu de caractères que l’argument de commande de l’URI peut prendre en charge sans avoir à coder ces caractères en pourcentage.</span><span class="sxs-lookup"><span data-stu-id="db336-219">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters. 
</span></span>
  
<span data-ttu-id="db336-220">Dans les segments < *command-argument* >, les caractères réservés dans le document RFC 3986 « : » et « / » font partie des données d’argument mais ne sont pas des délimiteurs, et sont donc inclus sans séquence d’échappement.</span><span class="sxs-lookup"><span data-stu-id="db336-220">Within <*command-argument*> segments the RFC 3986 reserved characters “:” and “/” are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="a-7-security-considerations"></a><span data-ttu-id="db336-221">A-7.</span><span class="sxs-lookup"><span data-stu-id="db336-221">A-7.</span></span> <span data-ttu-id="db336-222">Considérations relatives à la sécurité</span><span class="sxs-lookup"><span data-stu-id="db336-222">Security Considerations</span></span>

 <span data-ttu-id="db336-223">Sur les systèmes équipés de gestionnaires enregistrés, destinés à reconnaître et à effectuer les actions des URI ms-word, le fait de cliquer sur un lien vers un URI ms-word entraîne le lancement de l’application de traitement de texte enregistrée et demande à l’application de traitement de texte de tenter d’ouvrir un document situé à l’URI spécifié.</span><span class="sxs-lookup"><span data-stu-id="db336-223">
On systems that have registered handlers to recognize and act on ms-word URIs, clicking on a link to an ms-word URI will cause the registered word processing application to be launched, with instructions to the word processing application to attempt to open a document at the specified URI. Word processing applications registering to process ms-word URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.
</span></span> <span data-ttu-id="db336-224">Les applications de traitement de texte enregistrées, destinées à traiter des URI ms-word, doivent implémenter des protections pour empêcher l’ouverture de documents provenant de systèmes distants non approuvés pouvant inclure du code malveillant.</span><span class="sxs-lookup"><span data-stu-id="db336-224">Word processing applications registering to process ms-word URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span> 
  
### <a name="a-8-references"></a><span data-ttu-id="db336-225">A-8.</span><span class="sxs-lookup"><span data-stu-id="db336-225">A-8.	References</span></span> <span data-ttu-id="db336-226">Références</span><span class="sxs-lookup"><span data-stu-id="db336-226">References</span></span>

<span data-ttu-id="db336-227">RFC 3987 – International Resource Identifiers (IRIs)</span><span class="sxs-lookup"><span data-stu-id="db336-227">RFC 3987 – International Resource Identifiers (IRIs)
 
</span></span>  
  
## <a name="appendix-b---uri-scheme-registration-template-for-ms-powerpoint-scheme"></a><span data-ttu-id="db336-228">ANNEXE B – MODÈLE D’ENREGISTREMENT DES MODÈLES D’URI POUR LE MODÈLE MS-POWERPOINT</span><span class="sxs-lookup"><span data-stu-id="db336-228">APPENDIX B – URI SCHEME REGISTRATION TEMPLATE FOR MS-POWERPOINT SCHEME
</span></span>
<span data-ttu-id="db336-229"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="db336-229"></span></span>

### <a name="b-3-uri-scheme-syntax"></a><span data-ttu-id="db336-230">B-3.</span><span class="sxs-lookup"><span data-stu-id="db336-230">B-3.</span></span> <span data-ttu-id="db336-231">Syntaxe du modèle d’URI</span><span class="sxs-lookup"><span data-stu-id="db336-231">E-3.	URI Scheme Syntax</span></span>

- <span data-ttu-id="db336-232">Modèle pour PowerPoint 	= "ms-powerpoint:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="db336-232">PowerPoint Scheme 	=	“ms-powerpoint:” open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
</span></span>
    
- <span data-ttu-id="db336-233">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="db336-233">open-for-edit-cmd	= “ofe|u|” document-uri
</span></span>
    
- <span data-ttu-id="db336-234">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="db336-234">open-for-view-cmd	= “ofv|u|” document-uri</span></span>
    
- <span data-ttu-id="db336-235">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="db336-235">new-from-template-cmd = “nft|u|” template-uri [“|s|” save-location]</span></span>
    
- <span data-ttu-id="db336-236">document-uri = URI d’emplacement du document à ouvrir</span><span class="sxs-lookup"><span data-stu-id="db336-236">
document-uri	=	URI location of document to open</span></span>
    
- <span data-ttu-id="db336-237">template-uri = URI d’emplacement du modèle de fichier sur lequel le nouveau fichier sera basé</span><span class="sxs-lookup"><span data-stu-id="db336-237">template-uri	=	URI location of template file upon which new file will be based
</span></span>
    
- <span data-ttu-id="db336-238">save-location\* = URI d’emplacement du dossier dans lequel le nouveau document doit être créé</span><span class="sxs-lookup"><span data-stu-id="db336-238">save-location\*	= URI location of folder in which new document should be created</span></span>
    
- <span data-ttu-id="db336-239">\*save-location est un paramètre facultatif.</span><span class="sxs-lookup"><span data-stu-id="db336-239">\*save-location is an optional parameter</span></span>
    
### <a name="b-4-uri-scheme-semantics"></a><span data-ttu-id="db336-240">B-4.</span><span class="sxs-lookup"><span data-stu-id="db336-240">B-4.</span></span> <span data-ttu-id="db336-241">Sémantique du modèle d’URI</span><span class="sxs-lookup"><span data-stu-id="db336-241">H-4.	URI Scheme Semantics
</span></span>

<span data-ttu-id="db336-242">Le modèle ms-powerpoint définit une syntaxe d’URI pour l’ouverture et la création d’un document de présentation.</span><span class="sxs-lookup"><span data-stu-id="db336-242">The ms-powerpoint scheme defines a URI syntax for opening or creating a presentation document.</span></span> <span data-ttu-id="db336-243">Le modèle définit trois commandes qui indiquent les actions à effectuer avec le document référencé.</span><span class="sxs-lookup"><span data-stu-id="db336-243">The scheme defines three commands that serve as instructions regarding what should be done with the referenced document.</span></span> <span data-ttu-id="db336-244">Les commandes sont 1) open-for-edit-cmd (ofe), qui demande à une application de présentation d’ouvrir le document situé à l’URI spécifié pour modification ; 2) open-for-view-cmd (ofv), qui demande à une application de présentation d’ouvrir le document situé à l’URI spécifié en lecture seule ; et 3) new-from-template-cmd (nft), qui demande à une application de présentation de créer un document basé sur le modèle de document situé à l’URI template-uri spécifié et d’enregistrer le nouveau document à l’emplacement spécifié dans l’URI save-location facultatif ou, si cet URI facultatif n’a pas été spécifié, à l’emplacement de la bibliothèque de documents par défaut.</span><span class="sxs-lookup"><span data-stu-id="db336-244">The ms-powerpoint scheme defines a URI syntax for opening or creating a presentation document. The scheme defines three commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs a presentation application to open the document at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs a presentation application to open the document at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs a presentation application to create a new document based on the document template located at the specified template-uri URI and save the new document either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.
</span></span>
  
### <a name="b-5-applicationsprotocols-that-use-the-ms-powerpoint-uri-scheme"></a><span data-ttu-id="db336-245">B-5.</span><span class="sxs-lookup"><span data-stu-id="db336-245">B-5.</span></span> <span data-ttu-id="db336-246">Applications/Protocoles qui utilisent le modèle d’URI ms-powerpoint</span><span class="sxs-lookup"><span data-stu-id="db336-246">B-5.	Applications/Protocols that use the ms-powerpoint URI Scheme
</span></span>

<span data-ttu-id="db336-247">Microsoft Office 2013 utilise le modèle d’URI ms-powerpoint pour appeler Microsoft PowerPoint 2013 ou Microsoft PowerPoint 2010 avec Service Pack 2.</span><span class="sxs-lookup"><span data-stu-id="db336-247">The ms-powerpoint URI Scheme is used by Microsoft Office 2013 to invoke Microsoft PowerPoint 2013 or Microsoft PowerPoint 2010 with Service Pack 2. Microsoft SharePoint 2013 uses ms-powerpoint URIs as links to presentation documents stored in SharePoint document libraries.
</span></span> <span data-ttu-id="db336-248">Microsoft SharePoint 2013 utilise les URI ms-powerpoint pour rediriger vers des documents de présentation enregistrés dans les bibliothèques de documents SharePoint.</span><span class="sxs-lookup"><span data-stu-id="db336-248">Microsoft SharePoint 2013 uses ms-powerpoint URIs as links to presentation documents stored in SharePoint document libraries.</span></span>
  
### <a name="b-6-interoperability-considerations"></a><span data-ttu-id="db336-249">B-6.</span><span class="sxs-lookup"><span data-stu-id="db336-249">B-6.</span></span> <span data-ttu-id="db336-250">Considérations relatives à l’interopérabilité</span><span class="sxs-lookup"><span data-stu-id="db336-250">
G-6.	Interoperability Considerations 
</span></span>

<span data-ttu-id="db336-251">Notez que la barre verticale utilisée comme délimiteur dans cette spécification ne fait pas partie des caractères identifiés à la section 2.2 du RFC 3986 qui sont réservés à un usage éventuel comme délimiteurs.</span><span class="sxs-lookup"><span data-stu-id="db336-251">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters. 
</span></span> <span data-ttu-id="db336-252">Cette opération vise à optimiser le jeu de caractères que l’argument de commande de l’URI peut prendre en charge sans avoir à coder ces caractères en pourcentage.</span><span class="sxs-lookup"><span data-stu-id="db336-252">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters. 
</span></span>
  
<span data-ttu-id="db336-253">Dans les segments < *command-argument* >, les caractères réservés dans le document RFC 3986 « : » et « / » font partie des données d’argument mais ne sont pas des délimiteurs, et sont donc inclus sans séquence d’échappement.</span><span class="sxs-lookup"><span data-stu-id="db336-253">Within <*command-argument*> segments the RFC 3986 reserved characters “:” and “/” are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="b-7-security-considerations"></a><span data-ttu-id="db336-254">B-7.</span><span class="sxs-lookup"><span data-stu-id="db336-254">B-7.</span></span> <span data-ttu-id="db336-255">Considérations relatives à la sécurité</span><span class="sxs-lookup"><span data-stu-id="db336-255">Security Considerations</span></span>

<span data-ttu-id="db336-256">Sur les systèmes équipés de gestionnaires enregistrés, destinés à reconnaître et à effectuer les actions des URI ms-powerpoint, le fait de cliquer sur un lien vers un URI ms-powerpoint entraîne le lancement de l’application de présentation enregistrée et demande à l’application de tenter d’ouvrir un document situé à l’URI spécifié.</span><span class="sxs-lookup"><span data-stu-id="db336-256">On systems that have registered handlers to recognize and act on ms-powerpoint URIs, clicking on a link to an ms-powerpoint URI will cause the registered presentation application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-powerpoint URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.
</span></span> <span data-ttu-id="db336-257">Les applications enregistrées, destinées à traiter des URI ms-powerpoint, doivent implémenter des protections pour empêcher l’ouverture de documents provenant de systèmes distants non approuvés pouvant inclure du code malveillant.</span><span class="sxs-lookup"><span data-stu-id="db336-257">Applications registering to process ms-powerpoint URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="b-8-references"></a><span data-ttu-id="db336-258">B-8.</span><span class="sxs-lookup"><span data-stu-id="db336-258">B-8.	References
</span></span> <span data-ttu-id="db336-259">Références</span><span class="sxs-lookup"><span data-stu-id="db336-259">References</span></span>

<span data-ttu-id="db336-260">RFC 3987 – International Resource Identifiers (IRIs)</span><span class="sxs-lookup"><span data-stu-id="db336-260">RFC 3987 – International Resource Identifiers (IRIs)
 
</span></span>  
  
## <a name="appendix-c---uri-scheme-registration-template-for-ms-excel-scheme"></a><span data-ttu-id="db336-261">ANNEXE C – MODÈLE D’ENREGISTREMENT DES MODÈLES D’URI POUR LE MODÈLE MS-EXCEL</span><span class="sxs-lookup"><span data-stu-id="db336-261">APPENDIX C – URI SCHEME REGISTRATION TEMPLATE FOR MS-EXCEL SCHEME
</span></span>
<span data-ttu-id="db336-262"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="db336-262"></span></span>

### <a name="c-3-uri-scheme-syntax"></a><span data-ttu-id="db336-263">C-3.</span><span class="sxs-lookup"><span data-stu-id="db336-263">C-3.</span></span> <span data-ttu-id="db336-264">Syntaxe du modèle d’URI</span><span class="sxs-lookup"><span data-stu-id="db336-264">E-3.	URI Scheme Syntax</span></span>

> <span data-ttu-id="db336-265">Modèle pour Excel = "ms-excel:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="db336-265">Excel Scheme 	=	“ms-excel:” open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span></span>
    
> <span data-ttu-id="db336-266">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="db336-266">open-for-edit-cmd	= “ofe|u|” document-uri
</span></span>
    
> <span data-ttu-id="db336-267">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="db336-267">open-for-view-cmd	= “ofv|u|” document-uri</span></span>
    
> <span data-ttu-id="db336-268">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="db336-268">new-from-template-cmd = “nft|u|” template-uri [“|s|” save-location]</span></span>
    
> <span data-ttu-id="db336-269">document-uri = URI d’emplacement du document à ouvrir</span><span class="sxs-lookup"><span data-stu-id="db336-269">
document-uri	=	URI location of document to open</span></span>
    
> <span data-ttu-id="db336-270">template-uri = URI d’emplacement du modèle de fichier sur lequel le nouveau fichier sera basé</span><span class="sxs-lookup"><span data-stu-id="db336-270">template-uri	=	URI location of template file upon which new file will be based
</span></span>
    
> <span data-ttu-id="db336-271">save-location\* = URI d’emplacement du dossier dans lequel le nouveau document doit être créé</span><span class="sxs-lookup"><span data-stu-id="db336-271">save-location\*	= URI location of folder in which new document should be created</span></span>
    
> <span data-ttu-id="db336-272">\*save-location est un paramètre facultatif.</span><span class="sxs-lookup"><span data-stu-id="db336-272">\*save-location is an optional parameter</span></span>
    
### <a name="c-4-uri-scheme-semantics"></a><span data-ttu-id="db336-273">C-4.</span><span class="sxs-lookup"><span data-stu-id="db336-273">C-4.</span></span> <span data-ttu-id="db336-274">Sémantique du modèle d’URI</span><span class="sxs-lookup"><span data-stu-id="db336-274">H-4.	URI Scheme Semantics
</span></span>

<span data-ttu-id="db336-275">Le modèle ms-excel définit une syntaxe d’URI pour l’ouverture et la création d’un document de feuilles de calcul.</span><span class="sxs-lookup"><span data-stu-id="db336-275">The ms-excel scheme defines a URI syntax for opening or creating a spreadsheet document.</span></span> <span data-ttu-id="db336-276">Le modèle définit trois commandes qui indiquent les actions à effectuer avec le document référencé.</span><span class="sxs-lookup"><span data-stu-id="db336-276">The scheme defines three commands that serve as instructions regarding what should be done with the referenced document.</span></span> <span data-ttu-id="db336-277">Les commandes sont 1) open-for-edit-cmd (ofe), qui demande à une application de feuilles de calcul d’ouvrir le document situé à l’URI spécifié pour modification ; 2) open-for-view-cmd (ofv), qui demande à une application de feuilles de calcul d’ouvrir le document situé à l’URI spécifié en lecture seule ; et 3) new-from-template-cmd (nft), qui demande à une application de feuilles de calcul de créer un document basé sur le modèle de document situé à l’URI template-uri spécifié et d’enregistrer le nouveau document à l’emplacement spécifié dans l’URI save-location facultatif ou, si cet URI facultatif n’a pas été spécifié, à l’emplacement de la bibliothèque de documents par défaut.</span><span class="sxs-lookup"><span data-stu-id="db336-277">The ms-excel scheme defines a URI syntax for opening or creating a spreadsheet document. The scheme defines three commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs a spreadsheet application to open the document at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs a spreadsheet application to open the document at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs a spreadsheet application to create a new document based on the document template located at the specified template-uri URI and save the new document either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.
</span></span>
  
### <a name="c-5-applicationsprotocols-that-use-the-ms-excel-uri-scheme"></a><span data-ttu-id="db336-278">C-5.</span><span class="sxs-lookup"><span data-stu-id="db336-278">C-5.</span></span> <span data-ttu-id="db336-279">Applications/Protocoles qui utilisent le modèle d’URI ms-excel</span><span class="sxs-lookup"><span data-stu-id="db336-279">C-5.	Applications/Protocols that use the ms-excel URI Scheme
</span></span>

<span data-ttu-id="db336-280">Microsoft Office 2013 utilise le modèle d’URI ms-excel pour appeler Microsoft Excel 2013 ou Microsoft Excel 2010 avec Service Pack 2.</span><span class="sxs-lookup"><span data-stu-id="db336-280">The ms-excel URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Excel 2013 or Microsoft Excel 2010 with Service Pack 2. Microsoft SharePoint 2013 uses ms-excel URIs as links to spreadsheet documents stored in SharePoint document libraries.
</span></span> <span data-ttu-id="db336-281">Microsoft SharePoint 2013 utilise les URI ms-excel pour rediriger vers des documents de feuilles de calcul enregistrés dans les bibliothèques de documents SharePoint.</span><span class="sxs-lookup"><span data-stu-id="db336-281">Microsoft SharePoint 2013 uses ms-excel URIs as links to spreadsheet documents stored in SharePoint document libraries.</span></span>
  
### <a name="c-6-interoperability-considerations"></a><span data-ttu-id="db336-282">C-6.</span><span class="sxs-lookup"><span data-stu-id="db336-282">C-6.</span></span> <span data-ttu-id="db336-283">Considérations relatives à l’interopérabilité</span><span class="sxs-lookup"><span data-stu-id="db336-283">
G-6.	Interoperability Considerations 
</span></span>

<span data-ttu-id="db336-284">Notez que la barre verticale utilisée comme délimiteur dans cette spécification ne fait pas partie des caractères identifiés à la section 2.2 du RFC 3986 qui sont réservés à un usage éventuel comme délimiteurs.</span><span class="sxs-lookup"><span data-stu-id="db336-284">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters. 
</span></span> <span data-ttu-id="db336-285">Cette opération vise à optimiser le jeu de caractères que l’argument de commande de l’URI peut prendre en charge sans avoir à coder ces caractères en pourcentage.</span><span class="sxs-lookup"><span data-stu-id="db336-285">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters. 
</span></span>
  
<span data-ttu-id="db336-286">Dans les segments < *command-argument* >, les caractères réservés dans le document RFC 3986 « : » et « / » font partie des données d’argument mais ne sont pas des délimiteurs, et sont donc inclus sans séquence d’échappement.</span><span class="sxs-lookup"><span data-stu-id="db336-286">Within <*command-argument*> segments the RFC 3986 reserved characters “:” and “/” are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="c-7-security-considerations"></a><span data-ttu-id="db336-287">C-7.</span><span class="sxs-lookup"><span data-stu-id="db336-287">C-7.</span></span> <span data-ttu-id="db336-288">Considérations relatives à la sécurité</span><span class="sxs-lookup"><span data-stu-id="db336-288">Security Considerations</span></span>

<span data-ttu-id="db336-289">Sur les systèmes équipés de gestionnaires enregistrés, destinés à reconnaître et à effectuer les actions des URI ms-excel, le fait de cliquer sur un lien vers un URI ms-excel entraîne le lancement de l’application de feuilles de calcul enregistrée et demande à l’application de tenter d’ouvrir un document situé à l’URI spécifié.</span><span class="sxs-lookup"><span data-stu-id="db336-289">On systems that have registered handlers to recognize and act on ms-excel URIs, clicking on a link to an ms-excel URI will cause the registered spreadsheet application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-excel URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.
</span></span> <span data-ttu-id="db336-290">Les applications enregistrées, destinées à traiter des URI ms-excel, doivent implémenter des protections pour empêcher l’ouverture de documents provenant de systèmes distants non approuvés pouvant inclure du code malveillant.</span><span class="sxs-lookup"><span data-stu-id="db336-290">Applications registering to process ms-excel URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="c-8-references"></a><span data-ttu-id="db336-291">C-8.</span><span class="sxs-lookup"><span data-stu-id="db336-291">C-8.	References
</span></span> <span data-ttu-id="db336-292">Références</span><span class="sxs-lookup"><span data-stu-id="db336-292">References</span></span>

<span data-ttu-id="db336-293">RFC 3987 – International Resource Identifiers (IRIs)</span><span class="sxs-lookup"><span data-stu-id="db336-293">RFC 3987 – International Resource Identifiers (IRIs)
 
</span></span>  
  
## <a name="appendix-d---uri-scheme-registration-template-for-ms-visio-scheme"></a><span data-ttu-id="db336-294">ANNEXE D – MODÈLE D’ENREGISTREMENT DES MODÈLES D’URI POUR LE MODÈLE MS-VISIO</span><span class="sxs-lookup"><span data-stu-id="db336-294">APPENDIX D – URI SCHEME REGISTRATION TEMPLATE FOR MS-VISIO SCHEME
</span></span>
<span data-ttu-id="db336-295"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="db336-295"></span></span>

### <a name="d-3-uri-scheme-syntax"></a><span data-ttu-id="db336-296">D-3.</span><span class="sxs-lookup"><span data-stu-id="db336-296">D-3.</span></span> <span data-ttu-id="db336-297">Syntaxe du modèle d’URI</span><span class="sxs-lookup"><span data-stu-id="db336-297">E-3.	URI Scheme Syntax</span></span>

> <span data-ttu-id="db336-298">Modèle pour Visio = "ms-visio:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="db336-298">Visio Scheme 	=	“ms-visio:” open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
</span></span>
    
> <span data-ttu-id="db336-299">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="db336-299">open-for-edit-cmd	= “ofe|u|” document-uri
</span></span>
    
> <span data-ttu-id="db336-300">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="db336-300">open-for-view-cmd	= “ofv|u|” document-uri</span></span>
    
> <span data-ttu-id="db336-301">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="db336-301">new-from-template-cmd = “nft|u|” template-uri [“|s|” save-location]</span></span>
    
> <span data-ttu-id="db336-302">document-uri = URI d’emplacement du document à ouvrir</span><span class="sxs-lookup"><span data-stu-id="db336-302">
document-uri	=	URI location of document to open</span></span>
    
> <span data-ttu-id="db336-303">template-uri = URI d’emplacement du modèle de fichier sur lequel le nouveau fichier sera basé</span><span class="sxs-lookup"><span data-stu-id="db336-303">template-uri	=	URI location of template file upon which new file will be based
</span></span>
    
> <span data-ttu-id="db336-304">save-location\* = URI d’emplacement du dossier dans lequel le nouveau document doit être créé</span><span class="sxs-lookup"><span data-stu-id="db336-304">save-location\*	= URI location of folder in which new document should be created</span></span>
    
> <span data-ttu-id="db336-305">\*save-location est un paramètre facultatif.</span><span class="sxs-lookup"><span data-stu-id="db336-305">\*save-location is an optional parameter</span></span>
    
### <a name="d-4-uri-scheme-semantics"></a><span data-ttu-id="db336-306">D-4.</span><span class="sxs-lookup"><span data-stu-id="db336-306">D-4.</span></span> <span data-ttu-id="db336-307">Sémantique du modèle d’URI</span><span class="sxs-lookup"><span data-stu-id="db336-307">H-4.	URI Scheme Semantics
</span></span>

<span data-ttu-id="db336-308">Le modèle ms-visio définit une syntaxe d’URI pour l’ouverture et la création d’un document Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="db336-308">The ms-visio scheme defines a URI syntax for opening or creating a Microsoft Visio document.</span></span> <span data-ttu-id="db336-309">Le modèle définit trois commandes qui indiquent les actions à effectuer avec le document référencé.</span><span class="sxs-lookup"><span data-stu-id="db336-309">The scheme defines three commands that serve as instructions regarding what should be done with the referenced document.</span></span> <span data-ttu-id="db336-310">Les commandes sont 1) open-for-edit-cmd (ofe), qui demande à Visio d’ouvrir le document situé à l’URI spécifié pour modification ; 2) open-for-view-cmd (ofv), qui demande à Visio d’ouvrir le document situé à l’URI spécifié en lecture seule ; et 3) new-from-template-cmd (nft), qui demande à Visio de créer un document basé sur le modèle de document situé à l’URI template-uri spécifié et d’enregistrer le nouveau document à l’emplacement spécifié dans l’URI save-location facultatif ou, si cet URI facultatif n’a pas été spécifié, à l’emplacement de la bibliothèque de documents par défaut.</span><span class="sxs-lookup"><span data-stu-id="db336-310">The ms-visio scheme defines a URI syntax for opening or creating a Microsoft Visio document. The scheme defines three commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs Visio to open the document at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs Visio to open the document at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs Visio to create a new document based on the document template located at the specified template-uri URI and save the new document either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.
</span></span>
  
### <a name="d-5-applicationsprotocols-that-use-the-ms-visio-uri-scheme"></a><span data-ttu-id="db336-311">D-5.</span><span class="sxs-lookup"><span data-stu-id="db336-311">D-5.</span></span> <span data-ttu-id="db336-312">Applications/Protocoles qui utilisent le modèle d’URI ms-visio</span><span class="sxs-lookup"><span data-stu-id="db336-312">D-5.	Applications/Protocols that use the ms-visio URI Scheme
</span></span>

<span data-ttu-id="db336-313">Microsoft Office 2013 utilise le modèle d’URI ms-visio pour appeler Microsoft Visio 2013 ou Microsoft Visio 2010 avec Service Pack 2.</span><span class="sxs-lookup"><span data-stu-id="db336-313">The ms-visio URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Visio 2013 or Microsoft Visio 2010 with Service Pack 2. Microsoft SharePoint 2013 uses ms-visio URIs as links to Visio documents stored in SharePoint document libraries.
</span></span> <span data-ttu-id="db336-314">Microsoft SharePoint 2013 utilise les URI ms-visio pour rediriger vers des documents Visio enregistrés dans les bibliothèques de documents SharePoint.</span><span class="sxs-lookup"><span data-stu-id="db336-314">Microsoft SharePoint 2013 uses ms-visio URIs as links to Visio documents stored in SharePoint document libraries.</span></span>
  
### <a name="d-6-interoperability-considerations"></a><span data-ttu-id="db336-315">D-6.</span><span class="sxs-lookup"><span data-stu-id="db336-315">D-6.</span></span> <span data-ttu-id="db336-316">Considérations relatives à l’interopérabilité</span><span class="sxs-lookup"><span data-stu-id="db336-316">
G-6.	Interoperability Considerations 
</span></span>

<span data-ttu-id="db336-317">Notez que la barre verticale utilisée comme délimiteur dans cette spécification ne fait pas partie des caractères identifiés à la section 2.2 du RFC 3986 qui sont réservés à un usage éventuel comme délimiteurs.</span><span class="sxs-lookup"><span data-stu-id="db336-317">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters. 
</span></span> <span data-ttu-id="db336-318">Cette opération vise à optimiser le jeu de caractères que l’argument de commande de l’URI peut prendre en charge sans avoir à coder ces caractères en pourcentage.</span><span class="sxs-lookup"><span data-stu-id="db336-318">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters. 
</span></span>
  
<span data-ttu-id="db336-319">Dans les segments < *command-argument* >, les caractères réservés dans le document RFC 3986 « : » et « / » font partie des données d’argument mais ne sont pas des délimiteurs, et sont donc inclus sans séquence d’échappement.</span><span class="sxs-lookup"><span data-stu-id="db336-319">Within <*command-argument*> segments the RFC 3986 reserved characters “:” and “/” are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="d-7-security-considerations"></a><span data-ttu-id="db336-320">D-7.</span><span class="sxs-lookup"><span data-stu-id="db336-320">D-7.</span></span> <span data-ttu-id="db336-321">Considérations relatives à la sécurité</span><span class="sxs-lookup"><span data-stu-id="db336-321">Security Considerations</span></span>

<span data-ttu-id="db336-322">Sur les systèmes équipés de gestionnaires enregistrés, destinés à reconnaître et à effectuer les actions des URI ms-visio, le fait de cliquer sur un lien vers un URI ms-visio entraîne le lancement de l’application enregistrée et demande à l’application de tenter d’ouvrir un document situé à l’URI spécifié.</span><span class="sxs-lookup"><span data-stu-id="db336-322">On systems that have registered handlers to recognize and act on ms-visio URIs, clicking on a link to an ms-visio URI will cause the registered application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-visio URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.
</span></span> <span data-ttu-id="db336-323">Les applications enregistrées, destinées à traiter des URI ms-visio, doivent implémenter des protections pour empêcher l’ouverture de documents provenant de systèmes distants non approuvés pouvant inclure du code malveillant.</span><span class="sxs-lookup"><span data-stu-id="db336-323">Applications registering to process ms-visio URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="d-8-references"></a><span data-ttu-id="db336-324">D-8.</span><span class="sxs-lookup"><span data-stu-id="db336-324">D-8.	References
</span></span> <span data-ttu-id="db336-325">Références</span><span class="sxs-lookup"><span data-stu-id="db336-325">References</span></span>

<span data-ttu-id="db336-326">RFC 3987 – International Resource Identifiers (IRIs)</span><span class="sxs-lookup"><span data-stu-id="db336-326">RFC 3987 – International Resource Identifiers (IRIs)
 
</span></span>
  
## <a name="appendix-e---uri-scheme-registration-template-for-ms-access-scheme"></a><span data-ttu-id="db336-327">ANNEXE E – MODÈLE D’ENREGISTREMENT DES MODÈLES D’URI POUR LE MODÈLE MS-ACCESS</span><span class="sxs-lookup"><span data-stu-id="db336-327">APPENDIX E – URI SCHEME REGISTRATION TEMPLATE FOR MS-ACCESS SCHEME
</span></span>
<span data-ttu-id="db336-328"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="db336-328"></span></span>

### <a name="e-3-uri-scheme-syntax"></a><span data-ttu-id="db336-329">E-3.</span><span class="sxs-lookup"><span data-stu-id="db336-329">E-3.</span></span> <span data-ttu-id="db336-330">Syntaxe du modèle d’URI</span><span class="sxs-lookup"><span data-stu-id="db336-330">E-3.	URI Scheme Syntax</span></span>

> <span data-ttu-id="db336-331">Modèle pour Access = "ms-access:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="db336-331">Access Scheme 	=	“ms-access:” open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
</span></span>
    
> <span data-ttu-id="db336-332">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="db336-332">open-for-edit-cmd	= “ofe|u|” document-uri
</span></span>
    
> <span data-ttu-id="db336-333">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="db336-333">open-for-view-cmd	= “ofv|u|” document-uri</span></span>
    
> <span data-ttu-id="db336-334">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="db336-334">new-from-template-cmd = “nft|u|” template-uri [“|s|” save-location]</span></span>
    
> <span data-ttu-id="db336-335">document-uri = URI d’emplacement du document à ouvrir</span><span class="sxs-lookup"><span data-stu-id="db336-335">
document-uri	=	URI location of document to open</span></span>
    
> <span data-ttu-id="db336-336">template-uri = URI d’emplacement du modèle de fichier sur lequel le nouveau fichier sera basé</span><span class="sxs-lookup"><span data-stu-id="db336-336">template-uri	=	URI location of template file upon which new file will be based
</span></span>
    
> <span data-ttu-id="db336-337">save-location\* = URI d’emplacement du dossier dans lequel le nouveau document doit être créé</span><span class="sxs-lookup"><span data-stu-id="db336-337">save-location\*	= URI location of folder in which new document should be created</span></span>
    
> <span data-ttu-id="db336-338">\*save-location est un paramètre facultatif.</span><span class="sxs-lookup"><span data-stu-id="db336-338">\*save-location is an optional parameter</span></span>
    
### <a name="e-4-uri-scheme-semantics"></a><span data-ttu-id="db336-339">E-4.</span><span class="sxs-lookup"><span data-stu-id="db336-339">E-4.</span></span> <span data-ttu-id="db336-340">Sémantique du modèle d’URI</span><span class="sxs-lookup"><span data-stu-id="db336-340">H-4.	URI Scheme Semantics
</span></span>

<span data-ttu-id="db336-p158">Le modèle ms-access définit une syntaxe d’URI pour l’ouverture ou la création d’une base de données. Le modèle définit trois commandes qui font office d’instructions concernant les actions à effectuer avec le fichier de base de données. Les commandes sont 1) commande-ouvrir-pour-édition (ofe), qui donne l’instruction à l’application de base de données d’ouvrir la base de données située à l’URI spécifié pour édition ; 2) commande-ouvrir-pour-affichage (ofv), qui donne l’instruction à l’application de base de données d’ouvrir la base de données située à l’URI spécifié en mode lecture seule ; et 3) commande-créer-à-partir-d’un-modèle (nft), qui donne l’instruction à l’application de base de données de créer une base de données basée sur le modèle prédéfini situé à l’URI uri-du-modèle spécifié et d’enregistrer la nouvelle base de données dans l’emplacement spécifié dans l’URI emplacement-d’enregistrement facultatif ou, si cet URI facultatif n’a pas été spécifié, à l’emplacement de la bibliothèque de documents par défaut.</span><span class="sxs-lookup"><span data-stu-id="db336-p158">The ms-access scheme defines a URI syntax for opening or creating a database. The scheme defines three commands that serve as instructions regarding what should be done with the referenced database file. The commands are 1) open-for-edit-cmd (ofe), which instructs the database application to open the database at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs the database application to open the database at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs the database application to create a new database based on the template located at the specified template-uri URI and save the new database either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="e-5-applicationsprotocols-that-use-the-ms-access-uri-scheme"></a><span data-ttu-id="db336-344">E-5.</span><span class="sxs-lookup"><span data-stu-id="db336-344">E-5.</span></span> <span data-ttu-id="db336-345">Applications/Protocoles qui utilisent le modèle d’URI ms-access</span><span class="sxs-lookup"><span data-stu-id="db336-345">E-5.	 Applications/Protocols that use the ms-access URI Scheme
</span></span>

<span data-ttu-id="db336-346">Microsoft Office 2013 utilise le modèle d’URI ms-access pour appeler Microsoft Access 2013 ou Microsoft Access 2010 avec Service Pack 2 depuis des pages web.</span><span class="sxs-lookup"><span data-stu-id="db336-346">The ms-access URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Access 2013 or Microsoft Access 2010 with Service Pack 2 from web pages. Microsoft SharePoint 2013 uses ms-access URIs as links to Access databases stored in SharePoint document libraries.
</span></span> <span data-ttu-id="db336-347">Microsoft SharePoint 2013 utilise les URI ms-access pour rediriger vers des bases de données Access enregistrées dans les bibliothèques de documents SharePoint.</span><span class="sxs-lookup"><span data-stu-id="db336-347">Microsoft SharePoint 2013 uses ms-access URIs as links to Access databases stored in SharePoint document libraries.</span></span>
  
### <a name="e-6-interoperability-considerations"></a><span data-ttu-id="db336-348">E-6.</span><span class="sxs-lookup"><span data-stu-id="db336-348">E-6.</span></span> <span data-ttu-id="db336-349">Considérations relatives à l’interopérabilité</span><span class="sxs-lookup"><span data-stu-id="db336-349">
G-6.	Interoperability Considerations 
</span></span>

<span data-ttu-id="db336-350">Notez que la barre verticale utilisée comme délimiteur dans cette spécification ne fait pas partie des caractères identifiés à la section 2.2 du RFC 3986 qui sont réservés à un usage éventuel comme délimiteurs.</span><span class="sxs-lookup"><span data-stu-id="db336-350">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters. 
</span></span> <span data-ttu-id="db336-351">Cette opération vise à optimiser le jeu de caractères que l’argument de commande de l’URI peut prendre en charge sans avoir à coder ces caractères en pourcentage.</span><span class="sxs-lookup"><span data-stu-id="db336-351">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters. 
</span></span> <span data-ttu-id="db336-352">Dans les segments \<command-argument\>, les caractères réservés dans le document RFC 3986 « : » et « / » font partie des données d’argument mais ne sont pas des délimiteurs, et sont donc inclus sans séquence d’échappement.</span><span class="sxs-lookup"><span data-stu-id="db336-352">Within <command-argument> segments the RFC 3986 reserved characters “:” and “/” are part of the argument data, not delimiters, and are therefore included unescaped.</span></span>
  
### <a name="e-7-security-considerations"></a><span data-ttu-id="db336-353">E-7.</span><span class="sxs-lookup"><span data-stu-id="db336-353">E-7.</span></span> <span data-ttu-id="db336-354">Considérations relatives à la sécurité</span><span class="sxs-lookup"><span data-stu-id="db336-354">Security Considerations</span></span>

<span data-ttu-id="db336-355">Sur les systèmes équipés de gestionnaires enregistrés, destinés à reconnaître et à effectuer les actions des URI ms-access, le fait de cliquer sur un lien vers un URI ms-access entraîne le lancement de l’application enregistrée et demande à l’application de tenter d’ouvrir une base de données située à l’URI spécifié.</span><span class="sxs-lookup"><span data-stu-id="db336-355">On systems that have registered handlers to recognize and act on ms-access URIs, clicking on a link to an ms-access URI will cause the registered application to be launched, with instructions to the application to attempt to open a database at the specified URI. Applications registering to process ms-access URIs should implement protections to guard against opening databases from untrusted remote systems that may include malicious code.
</span></span> <span data-ttu-id="db336-356">Les applications enregistrées, destinées à traiter des URI ms-access doivent implémenter des protections pour empêcher l’ouverture de bases de données provenant de systèmes distants non approuvés pouvant inclure du code malveillant.</span><span class="sxs-lookup"><span data-stu-id="db336-356">Applications registering to process ms-access URIs should implement protections to guard against opening databases from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="e-8-references"></a><span data-ttu-id="db336-357">E-8.</span><span class="sxs-lookup"><span data-stu-id="db336-357">E-8.	References</span></span> <span data-ttu-id="db336-358">Références</span><span class="sxs-lookup"><span data-stu-id="db336-358">References</span></span>

<span data-ttu-id="db336-359">RFC 3987 – International Resource Identifiers (IRIs)</span><span class="sxs-lookup"><span data-stu-id="db336-359">RFC 3987 – International Resource Identifiers (IRIs)
 
</span></span>  
  
## <a name="appendix-f---uri-scheme-registration-template-for-ms-project-scheme"></a><span data-ttu-id="db336-360">ANNEXE F – MODÈLE D’ENREGISTREMENT DES MODÈLES D’URI POUR LE MODÈLE MS-PROJECT</span><span class="sxs-lookup"><span data-stu-id="db336-360">APPENDIX F – URI SCHEME REGISTRATION TEMPLATE FOR MS-PROJECT SCHEME
</span></span>
<span data-ttu-id="db336-361"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="db336-361"></span></span>

### <a name="f-3-uri-scheme-syntax"></a><span data-ttu-id="db336-362">F-3.</span><span class="sxs-lookup"><span data-stu-id="db336-362">F3</span></span> <span data-ttu-id="db336-363">Syntaxe du modèle d’URI</span><span class="sxs-lookup"><span data-stu-id="db336-363">E-3.	URI Scheme Syntax</span></span>

> <span data-ttu-id="db336-364">Modèle pour Project = "ms-project:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="db336-364">Project Scheme 	=	“ms-project:” open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
</span></span>
    
> <span data-ttu-id="db336-365">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="db336-365">open-for-edit-cmd	= “ofe|u|” document-uri
</span></span>
    
> <span data-ttu-id="db336-366">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="db336-366">open-for-view-cmd	= “ofv|u|” document-uri</span></span>
    
> <span data-ttu-id="db336-367">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="db336-367">new-from-template-cmd = “nft|u|” template-uri [“|s|” save-location]</span></span>
    
> <span data-ttu-id="db336-368">document-uri = URI d’emplacement du document à ouvrir</span><span class="sxs-lookup"><span data-stu-id="db336-368">
document-uri	=	URI location of document to open</span></span>
    
> <span data-ttu-id="db336-369">template-uri = URI d’emplacement du modèle de fichier sur lequel le nouveau fichier sera basé</span><span class="sxs-lookup"><span data-stu-id="db336-369">template-uri	=	URI location of template file upon which new file will be based
</span></span>
    
> <span data-ttu-id="db336-370">save-location\* = URI d’emplacement du dossier dans lequel le nouveau document doit être créé</span><span class="sxs-lookup"><span data-stu-id="db336-370">save-location\*	= URI location of folder in which new document should be created</span></span>
    
> <span data-ttu-id="db336-371">\*save-location est un paramètre facultatif.</span><span class="sxs-lookup"><span data-stu-id="db336-371">\*save-location is an optional parameter</span></span>
    
### <a name="f-4-uri-scheme-semantics"></a><span data-ttu-id="db336-372">F-4.</span><span class="sxs-lookup"><span data-stu-id="db336-372">F4</span></span> <span data-ttu-id="db336-373">Sémantique du modèle d’URI</span><span class="sxs-lookup"><span data-stu-id="db336-373">H-4.	URI Scheme Semantics
</span></span>

<span data-ttu-id="db336-374">Le modèle ms-project définit une syntaxe d’URI pour l’ouverture et la création d’un document Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="db336-374">The ms-project scheme defines a URI syntax for opening or creating a Microsoft Project document.</span></span> <span data-ttu-id="db336-375">Le modèle définit trois commandes qui indiquent les actions à effectuer avec le document référencé.</span><span class="sxs-lookup"><span data-stu-id="db336-375">The scheme defines three commands that serve as instructions regarding what should be done with the referenced document.</span></span> <span data-ttu-id="db336-376">Les commandes sont 1) open-for-edit-cmd (ofe), qui demande à Project d’ouvrir le document situé à l’URI spécifié pour modification ; 2) open-for-view-cmd (ofv), qui demande à Project d’ouvrir le document situé à l’URI spécifié en lecture seule ; et 3) new-from-template-cmd (nft), qui demande à Project de créer un document basé sur le modèle de document situé à l’URI template-uri spécifié et d’enregistrer le nouveau document à l’emplacement spécifié dans l’URI save-location facultatif ou, si cet URI facultatif n’a pas été spécifié, à l’emplacement de la bibliothèque de documents par défaut.</span><span class="sxs-lookup"><span data-stu-id="db336-376">The ms-project scheme defines a URI syntax for opening or creating a Microsoft Project document. The scheme defines three commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs Project to open the document at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs Project to open the document at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs Project to create a new document based on the document template located at the specified template-uri URI and save the new document either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.
</span></span>
  
### <a name="f-5-applicationsprotocols-that-use-the-ms-project-uri-scheme"></a><span data-ttu-id="db336-377">F-5.</span><span class="sxs-lookup"><span data-stu-id="db336-377">F5</span></span> <span data-ttu-id="db336-378">Applications/Protocoles qui utilisent le modèle d’URI ms-project</span><span class="sxs-lookup"><span data-stu-id="db336-378">F-5.	Applications/Protocols that use the ms-project URI Scheme
</span></span>

<span data-ttu-id="db336-379">Microsoft Office 2013 utilise le modèle d’URI ms-project pour appeler Microsoft Project 2013 depuis des pages web.</span><span class="sxs-lookup"><span data-stu-id="db336-379">The ms-project URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Project 2013 from web pages. Microsoft SharePoint 2013 uses ms-project URIs as links to Project documents stored in SharePoint document libraries.
</span></span> <span data-ttu-id="db336-380">Microsoft SharePoint 2013 utilise les URI ms-project pour rediriger vers des documents Project enregistrés dans les bibliothèques de documents SharePoint.</span><span class="sxs-lookup"><span data-stu-id="db336-380">The ms-project URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Project 2013 from web pages. Microsoft SharePoint 2013 uses ms-project URIs as links to Project documents stored in SharePoint document libraries.
</span></span>
  
### <a name="f-6-interoperability-considerations"></a><span data-ttu-id="db336-381">F-6.</span><span class="sxs-lookup"><span data-stu-id="db336-381">F6</span></span> <span data-ttu-id="db336-382">Considérations relatives à l’interopérabilité</span><span class="sxs-lookup"><span data-stu-id="db336-382">
G-6.	Interoperability Considerations 
</span></span>

<span data-ttu-id="db336-383">Notez que la barre verticale utilisée comme délimiteur dans cette spécification ne fait pas partie des caractères identifiés à la section 2.2 du RFC 3986 qui sont réservés à un usage éventuel comme délimiteurs.</span><span class="sxs-lookup"><span data-stu-id="db336-383">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters. 
</span></span> <span data-ttu-id="db336-384">Cette opération vise à optimiser le jeu de caractères que l’argument de commande de l’URI peut prendre en charge sans avoir à coder ces caractères en pourcentage.</span><span class="sxs-lookup"><span data-stu-id="db336-384">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters. 
</span></span>
  
<span data-ttu-id="db336-385">Dans les segments < *command-argument* >, les caractères réservés dans le document RFC 3986 « : » et « / » font partie des données d’argument mais ne sont pas des délimiteurs, et sont donc inclus sans séquence d’échappement.</span><span class="sxs-lookup"><span data-stu-id="db336-385">Within <*command-argument*> segments the RFC 3986 reserved characters “:” and “/” are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="f-7-security-considerations"></a><span data-ttu-id="db336-386">F-7.</span><span class="sxs-lookup"><span data-stu-id="db336-386">F7</span></span> <span data-ttu-id="db336-387">Considérations relatives à la sécurité</span><span class="sxs-lookup"><span data-stu-id="db336-387">Security Considerations</span></span>

<span data-ttu-id="db336-388">Sur les systèmes équipés de gestionnaires enregistrés, destinés à reconnaître et à effectuer les actions des URI ms-project, le fait de cliquer sur un lien vers un URI ms-project entraîne le lancement de l’application enregistrée et demande à l’application de tenter d’ouvrir un document situé à l’URI spécifié.</span><span class="sxs-lookup"><span data-stu-id="db336-388">On systems that have registered handlers to recognize and act on ms-project URIs, clicking on a link to an ms-project URI will cause the registered application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-project URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.
</span></span> <span data-ttu-id="db336-389">Les applications enregistrées, destinées à traiter des URI ms-project, doivent implémenter des protections pour empêcher l’ouverture de documents provenant de systèmes distants non approuvés pouvant inclure du code malveillant.</span><span class="sxs-lookup"><span data-stu-id="db336-389">Applications registering to process ms-project URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="f-8-references"></a><span data-ttu-id="db336-390">F-8.</span><span class="sxs-lookup"><span data-stu-id="db336-390">F8</span></span> <span data-ttu-id="db336-391">Références</span><span class="sxs-lookup"><span data-stu-id="db336-391">References</span></span>

<span data-ttu-id="db336-392">RFC 3987 – International Resource Identifiers (IRIs)</span><span class="sxs-lookup"><span data-stu-id="db336-392">RFC 3987 – International Resource Identifiers (IRIs)
 
</span></span>  
  
## <a name="appendix-g---uri-scheme-registration-template-for-ms-publisher-scheme"></a><span data-ttu-id="db336-393">ANNEXE G – MODÈLE D’ENREGISTREMENT DES MODÈLES D’URI POUR LE MODÈLE MS-PUBLISHER</span><span class="sxs-lookup"><span data-stu-id="db336-393">APPENDIX G – URI SCHEME REGISTRATION TEMPLATE FOR MS-PUBLISHER SCHEME
</span></span>
<span data-ttu-id="db336-394"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="db336-394"></span></span>

### <a name="g-3-uri-scheme"></a><span data-ttu-id="db336-395">G-3.</span><span class="sxs-lookup"><span data-stu-id="db336-395">G-3.</span></span> <span data-ttu-id="db336-396">Modèle d’URI</span><span class="sxs-lookup"><span data-stu-id="db336-396">G-3.	URI Scheme</span></span>

> <span data-ttu-id="db336-397">Modèle pour Publisher = "ms-publisher:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="db336-397">Syntax
Publisher Scheme 	=	“ms-publisher:” open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
</span></span>
    
> <span data-ttu-id="db336-398">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="db336-398">open-for-edit-cmd	= “ofe|u|” document-uri
</span></span>
    
> <span data-ttu-id="db336-399">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="db336-399">open-for-view-cmd	= “ofv|u|” document-uri</span></span>
    
> <span data-ttu-id="db336-400">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="db336-400">new-from-template-cmd = “nft|u|” template-uri [“|s|” save-location]</span></span>
    
> <span data-ttu-id="db336-401">document-uri = URI d’emplacement du document à ouvrir</span><span class="sxs-lookup"><span data-stu-id="db336-401">
document-uri	=	URI location of document to open</span></span>
    
> <span data-ttu-id="db336-402">template-uri = URI d’emplacement du modèle de fichier sur lequel le nouveau fichier sera basé</span><span class="sxs-lookup"><span data-stu-id="db336-402">template-uri	=	URI location of template file upon which new file will be based
</span></span>
    
> <span data-ttu-id="db336-403">save-location\* = URI d’emplacement du dossier dans lequel le nouveau document doit être créé</span><span class="sxs-lookup"><span data-stu-id="db336-403">save-location\*	= URI location of folder in which new document should be created</span></span>
    
> <span data-ttu-id="db336-404">\*save-location est un paramètre facultatif.</span><span class="sxs-lookup"><span data-stu-id="db336-404">\*save-location is an optional parameter</span></span>
    
### <a name="g-4-uri-scheme-semantics"></a><span data-ttu-id="db336-405">G-4.</span><span class="sxs-lookup"><span data-stu-id="db336-405">G-4.</span></span> <span data-ttu-id="db336-406">Sémantique du modèle d’URI</span><span class="sxs-lookup"><span data-stu-id="db336-406">H-4.	URI Scheme Semantics
</span></span>

<span data-ttu-id="db336-p178">Le modèle ms-publisher définit une syntaxe d’URI pour l’ouverture ou la création d’un document Microsoft Publisher. Le modèle définit trois commandes qui font office d’instructions concernant les actions à effectuer avec le document référencé. Les commandes sont 1) commande-ouvrir-pour-édition (ofe), qui donne l’instruction à Publisher d’ouvrir le document situé à l’URI spécifié pour édition ; 2) commande-ouvrir-pour-affichage (ofv), qui donne l’instruction à Publisher d’ouvrir le document situé à l’URI spécifié en mode lecture seule ; et 3) commande-créer-à-partir-d’un-modèle (nft), qui donne l’instruction à Publisher de créer un document basé sur le modèle prédéfini de document situé à l’URI uri-du-modèle spécifié et d’enregistrer le nouveau document dans l’emplacement spécifié dans l’URI emplacement-d’enregistrement facultatif ou, si cet URI facultatif n’a pas été spécifié, à l’emplacement de la bibliothèque de documents par défaut.</span><span class="sxs-lookup"><span data-stu-id="db336-p178">The ms-publisher scheme defines a URI syntax for opening or creating a Microsoft Publisher document. The scheme defines three commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs Publisher to open the document at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs Publisher to open the document at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs Publisher to create a new document based on the document template located at the specified template-uri URI and save the new document either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="g-5-applicationsprotocols-that-use-the-ms-publisher-uri-scheme"></a><span data-ttu-id="db336-410">G-5.</span><span class="sxs-lookup"><span data-stu-id="db336-410">G-5.</span></span> <span data-ttu-id="db336-411">Applications/Protocoles qui utilisent le modèle d’URI ms-publisher</span><span class="sxs-lookup"><span data-stu-id="db336-411">G-5.	Applications/Protocols that use the ms-publisher URI Scheme
</span></span>

<span data-ttu-id="db336-412">Microsoft Office 2013 utilise le modèle d’URI ms-publisher pour appeler Microsoft Publisher 2013 ou Microsoft Publisher 2010 avec Service Pack 2 depuis des pages web.</span><span class="sxs-lookup"><span data-stu-id="db336-412">The ms-publisher URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Publisher 2013 or Microsoft Publisher 2010 with Service Pack 2 from web pages. Microsoft SharePoint 2013 uses ms-publisher URIs as links to Publisher documents stored in SharePoint document libraries.
</span></span> <span data-ttu-id="db336-413">Microsoft SharePoint 2013 utilise les URI ms-publisher pour rediriger vers des documents Publisher enregistrés dans les bibliothèques de documents SharePoint.</span><span class="sxs-lookup"><span data-stu-id="db336-413">Microsoft SharePoint 2013 uses ms-publisher URIs as links to Publisher documents stored in SharePoint document libraries.</span></span>
  
### <a name="g-6-interoperability-considerations"></a><span data-ttu-id="db336-414">G-6.</span><span class="sxs-lookup"><span data-stu-id="db336-414">G-6.</span></span> <span data-ttu-id="db336-415">Considérations relatives à l’interopérabilité</span><span class="sxs-lookup"><span data-stu-id="db336-415">
G-6.	Interoperability Considerations 
</span></span>

<span data-ttu-id="db336-416">Notez que la barre verticale utilisée comme délimiteur dans cette spécification ne fait pas partie des caractères identifiés à la section 2.2 du RFC 3986 qui sont réservés à un usage éventuel comme délimiteurs.</span><span class="sxs-lookup"><span data-stu-id="db336-416">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters. 
</span></span> <span data-ttu-id="db336-417">Cette opération vise à optimiser le jeu de caractères que l’argument de commande de l’URI peut prendre en charge sans avoir à coder ces caractères en pourcentage.</span><span class="sxs-lookup"><span data-stu-id="db336-417">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters. 
</span></span> <span data-ttu-id="db336-418">Dans les segments \<command-argument\>, les caractères réservés dans le document RFC 3986 « : » et « / » font partie des données d’argument mais ne sont pas des délimiteurs, et sont donc inclus sans séquence d’échappement.</span><span class="sxs-lookup"><span data-stu-id="db336-418">Within <command-argument> segments the RFC 3986 reserved characters “:” and “/” are part of the argument data, not delimiters, and are therefore included unescaped.</span></span>
  
### <a name="g-7-security-considerations"></a><span data-ttu-id="db336-419">G-7.</span><span class="sxs-lookup"><span data-stu-id="db336-419">G-7.</span></span> <span data-ttu-id="db336-420">Considérations relatives à la sécurité</span><span class="sxs-lookup"><span data-stu-id="db336-420">Security Considerations</span></span>

<span data-ttu-id="db336-p184">Sur les systèmes qui ont enregistré des gestionnaires pour reconnaître et effectuer les actions des URI ms-publisher, le fait de cliquer sur un lien vers un URI ms-publisher entraîne le lancement de l’application enregistrée, avec des instructions pour que l’application tente d’ouvrir un document situé à l’URI spécifié. Les applications enregistrées pour traiter des URI ms-publisher doivent mettre en œuvre des protections pour empêcher l’ouverture de documents provenant de systèmes distants non approuvés pouvant inclure du code malveillant.</span><span class="sxs-lookup"><span data-stu-id="db336-p184">On systems that have registered handlers to recognize and act on ms-publisher URIs, clicking on a link to an ms-publisher URI will cause the registered application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-publisher URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="g-9-references"></a><span data-ttu-id="db336-423">G-9.</span><span class="sxs-lookup"><span data-stu-id="db336-423">G-9.	References</span></span> <span data-ttu-id="db336-424">Références</span><span class="sxs-lookup"><span data-stu-id="db336-424">References</span></span>

<span data-ttu-id="db336-425">RFC 3987 – International Resource Identifiers (IRIs)</span><span class="sxs-lookup"><span data-stu-id="db336-425">RFC 3987 – International Resource Identifiers (IRIs)
 
</span></span>  
  
## <a name="appendix-h---uri-scheme-registration-template-for-ms-spd-scheme"></a><span data-ttu-id="db336-426">ANNEXE H – MODÈLE D’ENREGISTREMENT DES MODÈLES D’URI POUR LE MODÈLE MS-SPD</span><span class="sxs-lookup"><span data-stu-id="db336-426">APPENDIX H – URI SCHEME REGISTRATION TEMPLATE FOR MS-SPD SCHEME
</span></span>
<span data-ttu-id="db336-427"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="db336-427"></span></span>

### <a name="h-3-uri-scheme-syntax"></a><span data-ttu-id="db336-428">H-3.</span><span class="sxs-lookup"><span data-stu-id="db336-428">H-3.</span></span> <span data-ttu-id="db336-429">Syntaxe du modèle d’URI</span><span class="sxs-lookup"><span data-stu-id="db336-429">E-3.	URI Scheme Syntax</span></span>

> <span data-ttu-id="db336-430">Modèle pour SharePoint Designer = "ms-spd:" open-for-edit-cmd</span><span class="sxs-lookup"><span data-stu-id="db336-430">SharePoint Designer Scheme 	=	“ms-spd:” open-for-edit-cmd 
</span></span>
    
> <span data-ttu-id="db336-431">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="db336-431">open-for-edit-cmd	= “ofe|u|” document-uri
</span></span>
    
> <span data-ttu-id="db336-432">document-uri = URI d’emplacement du document à ouvrir</span><span class="sxs-lookup"><span data-stu-id="db336-432">
document-uri	=	URI location of document to open</span></span>
    
### <a name="h-4-uri-scheme-semantics"></a><span data-ttu-id="db336-433">H-4.</span><span class="sxs-lookup"><span data-stu-id="db336-433">H-4.</span></span> <span data-ttu-id="db336-434">Sémantique du modèle d’URI</span><span class="sxs-lookup"><span data-stu-id="db336-434">H-4.	URI Scheme Semantics
</span></span>

<span data-ttu-id="db336-435">Le modèle ms-spd définit une syntaxe d’URI pour l’ouverture et la création d’un document Microsoft SharePoint Designer.</span><span class="sxs-lookup"><span data-stu-id="db336-435">The ms-spd scheme defines a URI syntax for opening a Microsoft SharePoint Designer document.</span></span> <span data-ttu-id="db336-436">Le modèle définit deux commandes qui indiquent les actions à effectuer avec le document référencé.</span><span class="sxs-lookup"><span data-stu-id="db336-436">The scheme defines two commands that serve as instructions regarding what should be done with the referenced document.</span></span> <span data-ttu-id="db336-437">Les commandes sont 1) open-for-edit-cmd (ofe), qui demande à SharePoint Designer d’ouvrir le document à l’URI spécifié pour modification ; et 2) open-for-view-cmd (ofv), qui demande à SharePoint Designer d’ouvrir le document à l’URI spécifié en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="db336-437">The ms-spd scheme defines a URI syntax for opening a Microsoft SharePoint Designer document. The scheme defines two commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs SharePoint Designer to open the document at the specified URI for editing; and 2) open-for-view-cmd (ofv), which instructs SharePoint Designer to open the document at the specified URI in a read-only mode.
</span></span>
  
### <a name="h-5-applicationsprotocols-that-use-the-ms-spd-uri-scheme"></a><span data-ttu-id="db336-438">H-5.</span><span class="sxs-lookup"><span data-stu-id="db336-438">H-5.</span></span> <span data-ttu-id="db336-439">Applications/Protocoles qui utilisent le modèle d’URI ms-spd</span><span class="sxs-lookup"><span data-stu-id="db336-439">H-5.	Applications/Protocols that use the ms-spd URI Scheme
</span></span>

<span data-ttu-id="db336-440">Microsoft Office 2013 utilise le modèle d’URI ms-spd pour appeler Microsoft SharePoint Designer 2013 depuis des pages web.</span><span class="sxs-lookup"><span data-stu-id="db336-440">The ms-spd URI Scheme is used by Microsoft Office 2013 to invoke Microsoft SharePoint Designer 2013 from web pages. Microsoft SharePoint 2013 uses ms-spd URIs as links to SharePoint Designer documents stored in SharePoint document libraries.
</span></span> <span data-ttu-id="db336-441">Microsoft SharePoint 2013 utilise les URI ms-spd pour rediriger vers des documents SharePoint Designer enregistrés dans les bibliothèques de documents SharePoint.</span><span class="sxs-lookup"><span data-stu-id="db336-441">The ms-spd URI Scheme is used by Microsoft Office 2013 to invoke Microsoft SharePoint Designer 2013 from web pages. Microsoft SharePoint 2013 uses ms-spd URIs as links to SharePoint Designer documents stored in SharePoint document libraries.
</span></span>
  
### <a name="h-6-interoperability-considerations"></a><span data-ttu-id="db336-442">H-6.</span><span class="sxs-lookup"><span data-stu-id="db336-442">H-6.</span></span> <span data-ttu-id="db336-443">Considérations relatives à l’interopérabilité</span><span class="sxs-lookup"><span data-stu-id="db336-443">
G-6.	Interoperability Considerations 
</span></span>

<span data-ttu-id="db336-444">Notez que la barre verticale utilisée comme délimiteur dans cette spécification ne fait pas partie des caractères identifiés à la section 2.2 du RFC 3986 qui sont réservés à un usage éventuel comme délimiteurs.</span><span class="sxs-lookup"><span data-stu-id="db336-444">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters. 
</span></span> <span data-ttu-id="db336-445">Cette opération vise à optimiser le jeu de caractères que l’argument de commande de l’URI peut prendre en charge sans avoir à coder ces caractères en pourcentage.</span><span class="sxs-lookup"><span data-stu-id="db336-445">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters. 
</span></span>
  
<span data-ttu-id="db336-446">Dans les segments < *command-argument* >, les caractères réservés dans le document RFC 3986 « : » et « / » font partie des données d’argument mais ne sont pas des délimiteurs, et sont donc inclus sans séquence d’échappement.</span><span class="sxs-lookup"><span data-stu-id="db336-446">Within <*command-argument*> segments the RFC 3986 reserved characters “:” and “/” are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="h-7-security-considerations"></a><span data-ttu-id="db336-447">H-7.</span><span class="sxs-lookup"><span data-stu-id="db336-447">H-7.</span></span> <span data-ttu-id="db336-448">Considérations relatives à la sécurité</span><span class="sxs-lookup"><span data-stu-id="db336-448">Security Considerations</span></span>

<span data-ttu-id="db336-449">Sur les systèmes équipés de gestionnaires enregistrés, destinés à reconnaître et à effectuer les actions des URI ms-spd, le fait de cliquer sur un lien vers un URI ms-spd entraîne le lancement de l’application enregistrée et demande à l’application de tenter d’ouvrir un document situé à l’URI spécifié.</span><span class="sxs-lookup"><span data-stu-id="db336-449">On systems that have registered handlers to recognize and act on ms-spd URIs, clicking on a link to an ms-spd URI will cause the registered application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-spd URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.
</span></span> <span data-ttu-id="db336-450">Les applications enregistrées, destinées à traiter des URI ms-spd, doivent implémenter des protections pour empêcher l’ouverture de documents provenant de systèmes distants non approuvés pouvant inclure du code malveillant.</span><span class="sxs-lookup"><span data-stu-id="db336-450">Applications registering to process ms-spd URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="h-8-references"></a><span data-ttu-id="db336-451">H-8.</span><span class="sxs-lookup"><span data-stu-id="db336-451">H-8.	References</span></span> <span data-ttu-id="db336-452">Références</span><span class="sxs-lookup"><span data-stu-id="db336-452">References</span></span>

<span data-ttu-id="db336-453">RFC 3987 – International Resource Identifiers (IRIs)</span><span class="sxs-lookup"><span data-stu-id="db336-453">RFC 3987 – International Resource Identifiers (IRIs)
 
</span></span>  
  
## <a name="appendix-i---uri-scheme-registration-template-for-ms-infopath-scheme"></a><span data-ttu-id="db336-454">ANNEXE I – MODÈLE D’ENREGISTREMENT DES MODÈLES D’URI POUR LE MODÈLE MS-INFOPATH</span><span class="sxs-lookup"><span data-stu-id="db336-454">APPENDIX I – URI SCHEME REGISTRATION TEMPLATE FOR MS-INFOPATH SCHEME
</span></span>
<span data-ttu-id="db336-455"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="db336-455"></span></span>

###   <a name="i-3-uri-scheme-syntax"></a><span data-ttu-id="db336-456">I-3.</span><span class="sxs-lookup"><span data-stu-id="db336-456">I-3.</span></span> <span data-ttu-id="db336-457">Syntaxe du modèle d’URI</span><span class="sxs-lookup"><span data-stu-id="db336-457">E-3.	URI Scheme Syntax</span></span>

> <span data-ttu-id="db336-458">Modèle pour Infopath = "ms-infopath:" open-for-edit-cmd | open-for-view-cmd</span><span class="sxs-lookup"><span data-stu-id="db336-458">Infopath Scheme 	=	“ms-infopath:” open-for-edit-cmd | open-for-view-cmd
</span></span>
    
> <span data-ttu-id="db336-459">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="db336-459">open-for-edit-cmd	= “ofe|u|” document-uri
</span></span>
    
> <span data-ttu-id="db336-460">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="db336-460">open-for-view-cmd	= “ofv|u|” document-uri</span></span>
    
> <span data-ttu-id="db336-461">document-uri = URI d’emplacement du document à ouvrir</span><span class="sxs-lookup"><span data-stu-id="db336-461">
document-uri	=	URI location of document to open</span></span>
    
### <a name="i-4-uri-scheme-semantics"></a><span data-ttu-id="db336-462">I-4.</span><span class="sxs-lookup"><span data-stu-id="db336-462">I-4.</span></span> <span data-ttu-id="db336-463">Sémantique du modèle d’URI</span><span class="sxs-lookup"><span data-stu-id="db336-463">H-4.	URI Scheme Semantics
</span></span>

<span data-ttu-id="db336-p198">Le modèle ms-infopath définit une syntaxe d’URI pour l’ouverture ou la création d’un document Microsoft Infopath. Le modèle définit deux commandes qui font office d’instructions concernant les actions à effectuer avec le document référencé. Les commandes sont 1) commande-ouvrir-pour-édition (ofe), qui donne l’instruction à Infopath d’ouvrir le document situé à l’URI spécifié pour édition ; 2) commande-ouvrir-pour-affichage (ofv), qui donne l’instruction à Infopath d’ouvrir le document situé à l’URI spécifié en mode lecture seule</span><span class="sxs-lookup"><span data-stu-id="db336-p198">The ms-infopath scheme defines a URI syntax for opening or creating a Microsoft Infopath document. The scheme defines two commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs Visio to open the document at the specified URI for editing; and 2) open-for-view-cmd (ofv), which instructs Visio to open the document at the specified URI in a read-only mode.</span></span>
  
### <a name="i-5-applicationsprotocols-that-use-the-ms-infopath-uri-scheme"></a><span data-ttu-id="db336-467">I-5.</span><span class="sxs-lookup"><span data-stu-id="db336-467">I-5.</span></span> <span data-ttu-id="db336-468">Applications/Protocoles qui utilisent le modèle d’URI ms-infopath</span><span class="sxs-lookup"><span data-stu-id="db336-468">I-5.	 Applications/Protocols that use the ms-infopath URI Scheme
</span></span>

<span data-ttu-id="db336-p200">Le modèle d’URI ms-infopath est utilisé par Microsoft Office 2013 pour appeler Microsoft Infopath 2013 à partir de pages web. Microsoft SharePoint 2013 utilise les URI ms-infopath comme des liens vers des documents Infopath stockés dans des bibliothèques de documents SharePoint.</span><span class="sxs-lookup"><span data-stu-id="db336-p200">The ms-infopath URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Infopath 2013 from web pages. Microsoft SharePoint 2013 uses ms-infopath URIs as links to Infopath documents stored in SharePoint document libraries.</span></span>
  
### <a name="i-6-interoperability-considerations"></a><span data-ttu-id="db336-471">I-6.</span><span class="sxs-lookup"><span data-stu-id="db336-471">I-6.</span></span> <span data-ttu-id="db336-472">Considérations relatives à l’interopérabilité</span><span class="sxs-lookup"><span data-stu-id="db336-472">
G-6.	Interoperability Considerations 
</span></span>

<span data-ttu-id="db336-473">Notez que la barre verticale utilisée comme délimiteur dans cette spécification ne fait pas partie des caractères identifiés à la section 2.2 du RFC 3986 qui sont réservés à un usage éventuel comme délimiteurs.</span><span class="sxs-lookup"><span data-stu-id="db336-473">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters. 
</span></span> <span data-ttu-id="db336-474">Cette opération vise à optimiser le jeu de caractères que l’argument de commande de l’URI peut prendre en charge sans avoir à coder ces caractères en pourcentage.</span><span class="sxs-lookup"><span data-stu-id="db336-474">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters. 
</span></span>
  
<span data-ttu-id="db336-475">Dans les segments < *command-argument* >, les caractères réservés dans le document RFC 3986 « : » et « / » font partie des données d’argument mais ne sont pas des délimiteurs, et sont donc inclus sans séquence d’échappement.</span><span class="sxs-lookup"><span data-stu-id="db336-475">Within <*command-argument*> segments the RFC 3986 reserved characters “:” and “/” are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="i-7-security-considerations"></a><span data-ttu-id="db336-476">I-7.</span><span class="sxs-lookup"><span data-stu-id="db336-476">I-7.</span></span> <span data-ttu-id="db336-477">Considérations relatives à la sécurité</span><span class="sxs-lookup"><span data-stu-id="db336-477">Security Considerations</span></span>

<span data-ttu-id="db336-478">Sur les systèmes équipés de gestionnaires enregistrés, destinés à reconnaître et à effectuer les actions des URI ms-infopath, le fait de cliquer sur un lien vers un URI ms-infopath entraîne le lancement de l’application enregistrée et demande à l’application de tenter d’ouvrir un document situé à l’URI spécifié.</span><span class="sxs-lookup"><span data-stu-id="db336-478">On systems that have registered handlers to recognize and act on ms-infopath URIs, clicking on a link to an ms-infopath URI will cause the registered application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-infopath URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.
</span></span> <span data-ttu-id="db336-479">Les applications enregistrées, destinées à traiter des URI ms-infopath, doivent implémenter des protections pour empêcher l’ouverture de documents provenant de systèmes distants non approuvés pouvant inclure du code malveillant.</span><span class="sxs-lookup"><span data-stu-id="db336-479">Applications registering to process ms-infopath URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="i-8-references"></a><span data-ttu-id="db336-480">I-8.</span><span class="sxs-lookup"><span data-stu-id="db336-480">I-8.	References</span></span> <span data-ttu-id="db336-481">Références</span><span class="sxs-lookup"><span data-stu-id="db336-481">References</span></span>

<span data-ttu-id="db336-482">RFC 3987 – International Resource Identifiers (IRIs)</span><span class="sxs-lookup"><span data-stu-id="db336-482">RFC 3987 – International Resource Identifiers (IRIs)
 
</span></span>  
  

