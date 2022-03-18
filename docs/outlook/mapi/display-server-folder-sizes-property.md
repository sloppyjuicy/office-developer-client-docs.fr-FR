---
title: Display Server Folder Sizes, propriété
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Display Server Folder Sizes Property
api_type:
- COM
ms.assetid: 38429fdb-be93-213a-a780-80f9837f55fa
description: Affiche la taille des dossiers spécifiés sur le serveur dans la boîte de dialogue Outlook taille du dossier.
ms.openlocfilehash: 67528116a38fd718e697e4128fd9c858b5abd383
ms.sourcegitcommit: 2d91bac3a93af3f1f73098f484000ba2a6377cf6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/17/2022
ms.locfileid: "63558682"
---
# <a name="display-server-folder-sizes-property"></a>Display Server Folder Sizes, propriété

**S’applique à** : Outlook 2013 | Outlook 2016
  
Affiche la taille des dossiers spécifiés sur le serveur dans la boîte de dialogue Outlook **taille** du dossier.
  
## <a name="quick-info"></a>Informations rapides

|**Informations**|**Valeur**|
|:-----|:-----|
|Exposé sur :  <br/> |[IMsgStore : objet IMAPIProp](imsgstoreimapiprop.md)  <br/> |
|Créé par :  <br/> |Fournisseur du Store  <br/> |
|Accessible par :  <br/> |Outlook clients et autres clients  <br/> |
|Type de propriété :  <br/> |PT_BOOLEAN  <br/> |
|Type d’accès :  <br/> |Lecture/écriture  <br/> |

## <a name="remarks"></a>Remarques

Pour fournir l’une des fonctionnalités du magasin, le fournisseur de magasin doit implémenter [IMAPIProp : IUnknown](imapipropiunknown.md) et renvoyer une balise de propriété valide pour l’une de ces propriétés transmises à un appel [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . Lorsque la balise de propriété de l’une de ces propriétés est transmise à [IMAPIProp::GetProps](imapiprop-getprops.md), le fournisseur de magasins doit également renvoyer la valeur de propriété correcte. Les fournisseurs du Store peuvent appeler [HrGetOneProp](hrgetoneprop.md) et [HrSetOneProp](hrsetoneprop.md) pour obtenir ou définir ces propriétés.
  
Pour récupérer la valeur de cette propriété, le client doit d’abord utiliser [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété, puis spécifier cette balise de propriété dans [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la valeur. Lorsque vous appelez [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), spécifiez les valeurs suivantes pour la structure [MAPINAMEID](mapinameid.md) pointée par le paramètre d’entrée _lppPropNames_ :
  
|**Structure**|**Valeur**|
|:-----|:-----|
|lpGuid:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulKind :  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName :  <br/> |L"urn:schemas-microsoft-com:office:outlook#serverfoldersizes »  <br/> |

Cette propriété est prise en charge dans Microsoft Outlook 2003 Service Pack (SP) 1. Si la version de Outlook est antérieure à Outlook 2003 SP 1 ou si sa valeur est **false**, Outlook affiche uniquement les tailles des dossiers dans la boutique locale. Si cette propriété est définie sur un magasin qui utilise Outlook 2003 SP 1, Outlook interrogera la taille de chaque dossier spécifié sur le serveur et le lecteur local.
  
Pour interroger la taille du dossier sur le serveur, Outlook ouvre un dossier dans la boutique avec [IMsgStore::OpenEntry](imsgstore-openentry.md), en passant **l’MAPI_NO_CACHE** d’indicateur, puis il interroge **PR_MESSAGE_SIZE_EXTENDED**. Le fournisseur de magasins doit ensuite renvoyer la taille du dossier sur le serveur.
  
Pour interroger la taille d’un dossier sur le lecteur local, Outlook ouvre le dossier sans **l’MAPI_NO_CACHE’indicateur**. Il recherche ensuite les **PR_MESSAGE_SIZE_EXTENDED** ; Le fournisseur de magasins doit renvoyer la taille du dossier spécifié sur le lecteur local.
  
Avec cette propriété définie, les fournisseurs de magasins qui synchronisent le contenu du magasin avec un serveur peuvent afficher les données de taille de dossier sur le serveur dans la boîte de dialogue taille **Outlook dossier.** Les utilisateurs peuvent ensuite comparer leur utilisation actuelle du stockage du serveur avec les quotas de serveur.
  
