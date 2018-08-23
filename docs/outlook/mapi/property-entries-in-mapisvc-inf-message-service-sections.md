---
title: Entrées de propriétés dans les sections de service de messagerie MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 714f99e2-80fc-4785-b707-611d8a6c229f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 038c13d24f3d797f7a4f8f9b7692240ce8004b74
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580333"
---
# <a name="property-entries-in-mapisvcinf-message-service-sections"></a>Entrées de propriétés dans les sections de service de messagerie MapiSvc.inf

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Entrées de définir les propriétés utilisent ce format :
  
 **balise de propriété** **=** valeur de la propriété 
  
La balise de propriété peut être une balise de propriété MAPI standard si les données de configuration représentent une des propriétés prédéfinies par MAPI, ou une balise non standard si les données ne représentent pas une propriété MAPI. La balise non standard est effectuée en combinant la valeur d’un identificateur de propriété avec un type de propriété. Le résultat est un nombre hexadécimal à 8 chiffres. La valeur de la propriété peut être tout ce qui est logique de la balise de propriété. 
  
Sections de service de message peuvent contenir plusieurs entrées selon le service de message en cours de configuration. Les propriétés MAPI suivantes sont généralement incluses dans une section de services de message dans le format de liste :
  
 **PR_DISPLAY_NAME** =  _chaîne_
  
 **PR_SERVICE_DLL_NAME** =  _nom de fichier DLL_
  
 **PR_SERVICE_ENTRY_NAME** =  _nom de la fonction de point d’entrée_
  
 **PR_SERVICE_SUPPORT_FILES** =  _liste des fichiers_
  
 **PR_SERVICE_DELETE_FILES** =  _liste des fichiers_
  
 **PR_RESOURCE_FLAGS** =  _masque de bits_
  
La chaîne **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) est le nom du service de message qui s’affiche dans l’interface utilisateur, le nom de l’utilisateur se connecte avec le service de message. Le nom complet est facultative dans mapisvc.inf. Parfois le nom complet est constitué de deux parties ; un composant affecté par le service de message et un composant attribué par l’utilisateur. Si l’utilisateur est responsable de l’affectation d’une des parties, il est généralement géré avec une boîte de dialogue spécial appelée une feuille de propriétés fournie par le service de message sous le contrôle d’une application cliente. 
  
Les informations fournies pour l’entrée **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) sont le nom de la DLL qui contient le service de message. Les informations fournies pour l’entrée **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) sont le nom de la fonction de point d’entrée dans cette DLL MAPI appelle pour configurer le service de message. 
  
Les fichiers répertoriés dans l’entrée **PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) sont des fichiers qui doivent être installés avec le service de message. De même, les fichiers dans l’entrée **PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) doivent être supprimés lorsque le service de message est supprimé. 
  
L’entrée **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) est une collection d’options définies pour le service de message. Par exemple, le bit SERVICE_SINGLE_COPY est défini lorsque le service de message ne peut apparaître qu’une seule fois dans un profil donné. Le bit SERVICE_NO_PRIMARY_IDENTITY est défini si le service de message ne fournit pas d’informations d’identité. 
  
Suivent de deux exemples d’entrées de propriété non standard. La première entrée spécifie le chemin d’accès au fichier utilisé par le carnet d’adresses par défaut en tant que valeur de la propriété ; la deuxième entrée spécifie une valeur de propriété numériques. Les deux entrées ont une signification spécifique pour le service Carnet d’adresses.
  
```cpp
6600001e=full path to file
66040003=integer

```


