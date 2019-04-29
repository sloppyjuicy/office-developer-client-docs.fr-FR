---
title: Masquer la propriété d'option de mise à jour de réunion
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ac7c891fa05560231a257f9bd52ccbbfe564b49d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412099"
---
# <a name="hide-meeting-update-option-property"></a>Masquer la propriété d'option de mise à jour de réunion

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Masque l'option permettant d'envoyer des mises à jour de réunion uniquement aux participants ajoutés ou supprimés.
  
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
|Kind. lpwstrName:  <br/> |L "urn: schemas-microsoft-com: Office: Outlook # allornonemtgupdatedlg"  <br/> |
   
Un fournisseur de banque qui utilise un serveur pour envoyer des mises à jour de réunion peut modifier la boîte **de dialogue Envoyer une mise à jour aux participants** . Cette fonctionnalité est utile car lorsque le serveur envoie une mise à jour de réunion, le serveur ne sait pas quels participants ont été ajoutés ou supprimés par l'utilisateur depuis la demande de réunion initiale. Lorsque cette propriété a la **valeur true**, l'option **Envoyer la mise à jour uniquement vers les participants ajoutés ou supprimés** n'est pas affichée dans la boîte de dialogue **Envoyer la mise à jour aux participants** . 
  
Cette propriété est ignorée si la version d'Outlook est antérieure à Microsoft Office Outlook 2003 Service Pack 1, ou si sa valeur **** est false.
  

