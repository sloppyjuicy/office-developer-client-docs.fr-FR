---
title: Masquer l’option De mise à jour de réunion, propriété
description: Cet article fournit une vue d’ensemble détaillée de la propriété d’option masquer la mise à jour de réunion avec des remarques supplémentaires.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Hide Meeting Update Option Property
api_type:
- COM
ms.assetid: 9e7b413f-a88a-a4ec-8d57-1f3058cce4a4
ms.openlocfilehash: c153b6f428f8ce71b94aa48521df5d60e2777f9c
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817514"
---
# <a name="hide-meeting-update-option-property"></a>Masquer l’option De mise à jour de réunion, propriété

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Masque l’option permettant d’envoyer des mises à jour de réunion uniquement aux participants ajoutés ou supprimés.
  
## <a name="quick-info"></a>Informations rapides

|Propriété |Valeur |
|:-----|:-----|
|Exposé sur :  <br/> |[IMsgStore : objet IMAPIProp](imsgstoreimapiprop.md)  <br/> |
|Créé par :  <br/> |Fournisseur du Store  <br/> |
|Accessible par :  <br/> |Outlook et d’autres clients  <br/> |
|Type de propriété :  <br/> |PT_BOOLEAN  <br/> |
|Type d’accès :  <br/> |Lecture/écriture  <br/> |
   
## <a name="remarks"></a>Remarques

Pour fournir l’une des fonctionnalités du magasin, le fournisseur de magasin doit implémenter [IMAPIProp : IUnknown](imapipropiunknown.md) et retourner une étiquette de propriété valide pour l’une de ces propriétés passées à un appel [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . Lorsque la balise de propriété pour l’une de ces propriétés est passée à [IMAPIProp::GetProps](imapiprop-getprops.md), le fournisseur de magasin doit également retourner la valeur de propriété correcte. Les fournisseurs du Store peuvent appeler [HrGetOneProp](hrgetoneprop.md) et [HrSetOneProp](hrsetoneprop.md) pour obtenir ou définir ces propriétés. 
  
Pour récupérer la valeur de cette propriété, le client doit d’abord utiliser [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété, puis spécifier cette balise de propriété dans [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la valeur. Lors de l’appel [d’IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), spécifiez les valeurs suivantes pour la structure [MAPINAMEID](mapinameid.md) pointée par le paramètre  _d’entrée lppPropNames_ :
  
|Propriété |Valeur |
|:-----|:-----|
|lpGuid :  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulKind :  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName :  <br/> |L"urn:schemas-microsoft-com:office:outlook#allornonemtgupdatedlg »  <br/> |
   
Un fournisseur de magasin qui utilise un serveur pour envoyer des mises à jour de réunion peut modifier la boîte **de dialogue Envoyer la mise à jour aux participants** . Cette fonctionnalité est utile, car lorsque le serveur envoie une mise à jour de réunion, le serveur ne sait pas quels participants ont été ajoutés ou supprimés par l’utilisateur depuis la demande de réunion initiale. Lorsque cette propriété a la **valeur true**, l’option **Envoyer la mise à jour uniquement aux participants ajoutés ou supprimés** n’est pas affichée dans la boîte de dialogue **Envoyer la mise à jour aux participants** . 
  
Cette propriété est ignorée si la version de Outlook est antérieure à Microsoft Office Outlook Service Pack 1 2003 ou si sa valeur est **false**.
  

