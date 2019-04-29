---
title: Propriété d'affichage des tailles de dossier du serveur
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 85a8b5216eac1dd4e4cebd1313cb31c9b5d70227
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434549"
---
# <a name="display-server-folder-sizes-property"></a>Propriété d'affichage des tailles de dossier du serveur

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Affiche les tailles des dossiers spécifiés sur le serveur dans la boîte de dialogue **taille du dossier** Outlook. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Exposé sur:  <br/> |[IMsgStore: objet IMAPIProp](imsgstoreimapiprop.md)  <br/> |
|Créé par:  <br/> |Fournisseur de magasin  <br/> |
|Accès par:  <br/> |Outlook et d'autres clients  <br/> |
|Type de propriété:  <br/> |PT_BOOLEAN  <br/> |
|Type d'accès:  <br/> |Lecture/écriture  <br/> |
   
## <a name="remarks"></a>Remarques

Pour fournir l'une des fonctionnalités de magasin, le fournisseur de banque doit implémenter [IMAPIProp: IUnknown](imapipropiunknown.md) et renvoyer une balise de propriété valide pour l'une des propriétés transmises à un appel [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) . Lorsque la balise de propriété de l'une de ces propriétés est transmise à [IMAPIProp:: GetProps](imapiprop-getprops.md), le fournisseur Store doit également renvoyer la valeur de propriété correcte. Les fournisseurs de magasins peuvent appeler [HrGetOneProp](hrgetoneprop.md) et [HrSetOneProp](hrsetoneprop.md) pour obtenir ou définir ces propriétés. 
  
Pour récupérer la valeur de cette propriété, le client doit d'abord utiliser [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété, puis spécifier cette balise de propriété dans [IMAPIProp:: GetProps](imapiprop-getprops.md) pour obtenir la valeur. Lors de l'appel de [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md), spécifiez les valeurs suivantes pour la structure [MAPINAMEID](mapinameid.md) pointée par le paramètre d'entrée _lppPropNames_:
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind. lpwstrName:  <br/> |L "urn: schemas-microsoft-com: Office: Outlook # serverfoldersizes"  <br/> |
   
Cette propriété est prise en charge dans Microsoft Outlook 2003 Service Pack (SP) 1. Si la version d'Outlook est antérieure à Outlook 2003 SP 1, ou si sa valeur est **false**, Outlook affiche uniquement la taille des dossiers sur le magasin local. Si cette propriété est définie sur un magasin qui utilise Outlook 2003 SP 1, Outlook demande la taille de chaque dossier spécifié sur le serveur et sur le lecteur local. 
  
Pour rechercher la taille du dossier sur le serveur, Outlook ouvre un dossier sur le magasin avec [IMsgStore:: OpenEntry](imsgstore-openentry.md), en transmettant l'indicateur **MAPI_NO_CACHE**, puis il interroge **PR_MESSAGE_SIZE_EXTENDED**. Le fournisseur de banque doit ensuite renvoyer la taille du dossier sur le serveur.
  
Pour rechercher la taille d'un dossier sur le lecteur local, Outlook ouvre le dossier sans l'indicateur **MAPI_NO_CACHE** . Il interroge ensuite **PR_MESSAGE_SIZE_EXTENDED**; le fournisseur de la Banque doit renvoyer la taille du dossier spécifié sur le lecteur local.
  
Avec ce jeu de propriétés, les fournisseurs de magasin qui synchronisent le contenu du magasin sur un serveur peuvent afficher les données de taille de dossier sur le serveur dans la boîte de dialogue **taille du dossier** Outlook. Les utilisateurs peuvent ensuite comparer leur utilisation de stockage de serveur actuelle avec des quotas de serveur. 
  

