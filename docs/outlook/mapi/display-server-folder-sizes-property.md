---
title: Propriété tailles du dossier d’affichage Server
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Display Server Folder Sizes Property
api_type:
- COM
ms.assetid: 38429fdb-be93-213a-a780-80f9837f55fa
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 1ddf4501918d598169a3a74fd1c8d2ac38499cd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783175"
---
# <a name="display-server-folder-sizes-property"></a>Propriété tailles du dossier d’affichage Server

  
  
**S’applique à**: Outlook 
  
Affiche la taille des dossiers spécifiés sur le serveur dans la boîte de dialogue Outlook **Taille du dossier** . 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Exposée sur :  <br/> |[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) objet  <br/> |
|Créé par :  <br/> |Fournisseur de banque  <br/> |
|Accessible par :  <br/> |Outlook et autres clients  <br/> |
|Type de propriété :  <br/> |PT_BOOLEAN  <br/> |
|Type d’accès :  <br/> |En lecture-écriture.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour fournir une des fonctionnalités de magasin, le fournisseur de banque doit implémenter [IMAPIProp : IUnknown](imapipropiunknown.md) et renvoyer une balise de propriété valide pour une de ces propriétés passées à un appel [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . Lorsque la balise de propriété pour une de ces propriétés est transmise à [IMAPIProp::GetProps](imapiprop-getprops.md), le fournisseur de banque doit également retourner la valeur de la propriété adéquate. Fournisseurs de magasins peuvent appeler [HrGetOneProp](hrgetoneprop.md) et [HrSetOneProp](hrsetoneprop.md) pour obtenir ou définir ces propriétés. 
  
Pour récupérer la valeur de cette propriété, le client doit d’abord utiliser [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété, puis spécifiez cette balise de propriété dans [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la valeur. Lors de l’appel [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), spécifiez les valeurs suivantes pour la structure [MAPINAMEID](mapinameid.md) sur laquelle pointé le paramètre d’entrée _lppPropNames_:
  
|||
|:-----|:-----|
|lpGuid :  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulKind :  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName :  <br/> |L « urn : schemas-microsoft-com:office:outlook #serverfoldersizes »  <br/> |
   
Cette propriété est prise en charge dans Microsoft Outlook 2003 Service Pack (SP) 1. Si la version d’Outlook est antérieure à Outlook 2003 Service Pack 1, ou si sa valeur est **false**, Outlook affiche uniquement les tailles des dossiers dans le magasin local. Si cette propriété est définie sur un magasin qui utilise Outlook 2003 Service Pack 1, Outlook interroge la taille de chaque dossier spécifié sur le serveur et le disque local. 
  
Pour rechercher la taille du dossier sur le serveur, Outlook ouvre un dossier sur le magasin avec [IMsgStore::OpenEntry](imsgstore-openentry.md), en passant l’indicateur **MAPI_NO_CACHE**, et il interroge pour **PR_MESSAGE_SIZE_EXTENDED**. Le fournisseur de banque doit ensuite retourner la taille du dossier sur le serveur.
  
Pour rechercher la taille d’un dossier sur le disque local, Outlook ouvre le dossier sans l’indicateur **MAPI_NO_CACHE** . Il interroge **PR_MESSAGE_SIZE_EXTENDED**; ensuite le fournisseur de banque doit renvoyer la taille du dossier spécifié sur le disque local.
  
Avec ce jeu de propriétés, les fournisseurs de magasins synchroniser le magasin de contenu vers un serveur peuvent afficher des données de taille de dossier sur le serveur dans la boîte de dialogue Outlook **Taille du dossier** . Les utilisateurs peuvent comparer puis leur utilisation actuelle de stockage serveur avec des quotas de serveur. 
  

