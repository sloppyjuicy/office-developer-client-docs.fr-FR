---
title: Masquer la propriété de Option de mise à jour de réunion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Hide Meeting Update Option Property
api_type:
- COM
ms.assetid: 9e7b413f-a88a-a4ec-8d57-1f3058cce4a4
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 25942df6f6156266f16cf6e681270dbb530472e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783453"
---
# <a name="hide-meeting-update-option-property"></a>Masquer la propriété de Option de mise à jour de réunion

  
  
**S’applique à**: Outlook 
  
Masque l’option Envoyer des mises à jour de réunion pour seulement les participants ajoutés ou supprimés.
  
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
|Kind.lpwstrName :  <br/> |L « urn : schemas-microsoft-com:office:outlook #allornonemtgupdatedlg »  <br/> |
   
Un fournisseur de magasins qui utilise un serveur pour envoyer des mises à jour de réunion permettre modifier la boîte de dialogue **Envoyer la mise à jour aux participants** . Cette fonctionnalité est utile car lorsque le serveur envoie une mise à jour de la réunion, le serveur ne sait pas les participants ont été ajoutés ou supprimés par l’utilisateur par rapport à la demande de réunion initiale. Lorsque cette propriété a la **valeur true**, l’option **Envoyer des mises à jour uniquement aux participants ajoutés ou supprimés** s’affiche pas dans la boîte de dialogue **Envoyer la mise à jour aux participants** . 
  
Cette propriété est ignorée si la version d’Outlook est antérieure à Microsoft Office Outlook 2003 Service Pack 1, ou si sa valeur est **false**.
  

