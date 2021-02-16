---
title: Entrées de propriété dans les sections du service de message MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 714f99e2-80fc-4785-b707-611d8a6c229f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ad2732f2f8dba4f506318a1b6faefb617a60584a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427996"
---
# <a name="property-entries-in-mapisvcinf-message-service-sections"></a>Entrées de propriété dans les sections du service de message MapiSvc.inf

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les entrées qui définissent des propriétés utilisent ce format :
  
 **balise de propriété** **=** valeur de la propriété 
  
La balise de propriété peut être une balise de propriété MAPI standard si les données de configuration représentent l’une des propriétés prédéfinie par MAPI ou une balise non standard si les données ne représentent pas une propriété MAPI. La balise nonstandard est réalisée en combinant la valeur d’un identificateur de propriété avec un type de propriété. Le résultat est un nombre hexadécimal à 8 chiffres. La valeur de la propriété peut être tout ce qui est logique pour la balise de propriété. 
  
Les sections du service de message peuvent contenir une variété d’entrées selon le service de message configuré. Les propriétés MAPI suivantes sont généralement incluses dans une section de services de message au format répertorié :
  
 **PR_DISPLAY_NAME**  =   _string_
  
 **PR_SERVICE_DLL_NAME**  =   _nom du fichier DLL_
  
 **PR_SERVICE_ENTRY_NAME**  =   _nom de la fonction de point d’entrée_
  
 **PR_SERVICE_SUPPORT_FILES**  =   _liste des fichiers_
  
 **PR_SERVICE_DELETE_FILES**  =   _liste des fichiers_
  
 **PR_RESOURCE_FLAGS**  =   _masque de bits_
  
La **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) est le nom du service de message affiché dans l’interface utilisateur, le nom que l’utilisateur associe au service de message. Le nom complet est une entrée facultative dans mapisvc.inf. Parfois, le nom complet est composé de deux parties . une partie affectée par le service de message et une partie affectée par l’utilisateur; Si l’utilisateur est responsable de l’affectation de l’un des composants, cela est généralement géré avec une boîte de dialogue spéciale appelée feuille de propriétés fournie par le service de message sous le contrôle d’une application cliente. 
  
Les informations fournies pour **l’entrée PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) sont le nom de la DLL qui contient le service de message. Les informations fournies pour l’entrée **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) sont le nom de la fonction de point d’entrée dans cette DLL que MAPI appelle pour configurer le service de message. 
  
Les fichiers répertoriés dans **l’entrée PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) sont des fichiers qui doivent être installés avec le service de message. De même, les fichiers de **l’PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) doivent être supprimés lorsque le service de message est supprimé. 
  
**L PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) est une collection d’options définies pour le service de message. Par exemple, le bit SERVICE_SINGLE_COPY est définie lorsque le service de message ne peut apparaître qu’une seule fois dans un profil donné. Le bit SERVICE_NO_PRIMARY_IDENTITY est définie si le service de message ne fournit pas d’informations d’identité. 
  
Deux exemples d’entrées de propriété non normes suivent. La première entrée spécifie le chemin d’accès au fichier utilisé par le carnet d’adresses par défaut comme valeur de propriété ; la deuxième entrée spécifie une valeur de propriété numérique. Les deux entrées ont une signification spécifique au service de message AB.
  
```cpp
6600001e=full path to file
66040003=integer

```


