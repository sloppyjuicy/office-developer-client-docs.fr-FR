---
title: Entrées de propriétés dans les sections de service de messagerie MapiSvc. inf
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
# <a name="property-entries-in-mapisvcinf-message-service-sections"></a>Entrées de propriétés dans les sections de service de messagerie MapiSvc. inf

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les entrées qui définissent les propriétés utilisent ce format:
  
 **balise de propriété** **=** valeur de la propriété 
  
La balise property peut être une balise de propriété MAPI standard si les données de configuration représentent une des propriétés prédéfinies par MAPI, ou une balise non standard si les données ne représentent pas une propriété MAPI. La balise non standard est créée en associant la valeur d'un identificateur de propriété à un type de propriété. Le résultat est un nombre hexadécimal à 8 chiffres. La valeur de la propriété peut être quelque peu significative pour la balise de propriété. 
  
Les sections de service de messagerie peuvent contenir plusieurs entrées en fonction du service de messagerie en cours de configuration. Les propriétés MAPI suivantes sont généralement incluses dans une section services de messagerie dans le format répertorié:
  
 **** =  _Chaîne_ PR_DISPLAY_NAME
  
 **PR_SERVICE_DLL_NAME** =  _nom du fichier dll_
  
 **PR_SERVICE_ENTRY_NAME** =  _nom de la fonction de point d'entrée_
  
 **** =  _Liste de fichiers_ PR_SERVICE_SUPPORT_FILES
  
 **** =  _Liste de fichiers_ PR_SERVICE_DELETE_FILES
  
 **** =  _Masque_ de PR_RESOURCE_FLAGS
  
La chaîne **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) est le nom du service de messagerie qui est affiché dans l'interface utilisateur, le nom que l'utilisateur associe au service de messagerie. Le nom complet est une entrée facultative dans MAPISVC. inf. Parfois, le nom complet est composé de deux parties; un composant affecté par le service de messagerie et un composant attribué par l'utilisateur. Si l'utilisateur est responsable de l'affectation de l'un des composants, cette opération est généralement gérée à l'aide d'une boîte de dialogue spéciale appelée feuille de propriétés fournie par le service de messagerie sous le contrôle d'une application cliente. 
  
Les informations fournies pour l'entrée **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) sont le nom de la dll qui contient le service de messagerie. Les informations fournies pour l'entrée **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) sont le nom de la fonction de point d'entrée au sein de cette dll qu'MAPI appelle pour configurer le service de messagerie. 
  
Les fichiers répertoriés dans l'entrée **PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) sont des fichiers qui doivent être installés avec le service de messagerie. De même, les fichiers de l'entrée **PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) doivent être supprimés lors de la suppression du service de messagerie. 
  
L'entrée **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) est une collection d'options définies pour le service de messagerie. Par exemple, le bit SERVICE_SINGLE_COPY est défini lorsque le service de messagerie ne peut apparaître qu'une seule fois dans un profil donné. Le bit SERVICE_NO_PRIMARY_IDENTITY est défini si le service de message ne fournit pas d'informations d'identité. 
  
Deux exemples d'entrées de propriétés non standard suivent. La première entrée spécifie le chemin d'accès au fichier utilisé par le carnet d'adresses par défaut comme valeur de la propriété; la deuxième entrée spécifie une valeur de propriété numérique. Les deux entrées ont une signification spécifique pour le service de messagerie du carnet d'ADR.
  
```cpp
6600001e=full path to file
66040003=integer

```


