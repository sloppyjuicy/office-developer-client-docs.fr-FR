---
title: Make Store Type Private, propriété
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Make Store Type Private Property
api_type:
- COM
ms.assetid: 7f489f55-46d4-8a88-6ebe-9db6446e69a5
description: Traite un magasin secondaire comme privé. Un fournisseur de banque d’informations peut utiliser cette propriété Outlook la traiter comme privée lorsqu’il s’agit d’un magasin secondaire pour un utilisateur.
ms.openlocfilehash: a1426ec8ebaf9e2613576b7ff9b45c155e929934
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63762535"
---
# <a name="make-store-type-private-property"></a>Make Store Type Private, propriété

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Traite un magasin secondaire comme privé.
  
## <a name="quick-info"></a>Informations rapides

|Propriété |Valeur |
|:-----|:-----|
|Exposé sur :  <br/> |[IMsgStore : objet IMAPIProp](imsgstoreimapiprop.md)  <br/> |
|Créé par :  <br/> |Fournisseur du Store  <br/> |
|Accessible par :  <br/> |Outlook clients et autres clients  <br/> |
|Type de propriété :  <br/> |PT_BOOLEAN  <br/> |
|Type d’accès :  <br/> |Lecture/écriture  <br/> |
   
## <a name="remarks"></a>Remarques

Pour fournir l’une des fonctionnalités du magasin, le fournisseur de magasin doit implémenter [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) et renvoyer une balise de propriété valide pour l’une de ces propriétés transmises à un appel [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . Lorsque la balise de propriété de l’une de ces propriétés est transmise à [IMAPIProp::GetProps](imapiprop-getprops.md), le fournisseur de magasins doit également renvoyer la valeur de propriété correcte. Les fournisseurs du Store peuvent appeler [HrGetOneProp](hrgetoneprop.md) et [HrSetOneProp](hrsetoneprop.md) pour obtenir ou définir ces propriétés. 
  
Pour récupérer la valeur de cette propriété, le client doit d’abord utiliser [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété, puis spécifier cette balise de propriété dans [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la valeur. Lorsque vous appelez [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), spécifiez les valeurs suivantes pour la structure [MAPINAMEID](mapinameid.md) pointée par le paramètre d’entrée  _lppPropNames_ :
  
|Propriété |Valeur |
|:-----|:-----|
|lpGuid:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulKind :  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName :  <br/> |L"urn:schemas-microsoft-com:office:outlook#storetypeprivate »  <br/> |
   
Un fournisseur de banque d’informations peut utiliser cette propriété Outlook la traiter comme privée lorsqu’il s’agit d’un magasin secondaire pour un utilisateur. 
  
Par défaut, Outlook traite une banque secondaire de la même manière qu’un magasin de délégués, et les éléments de la banque secondaire sont privés uniquement si l’utilisateur les marque spécifiquement comme privés. Lorsque cette propriété a **la valeur True**, les éléments supprimés d’une magasin secondaire  sont déplacés vers le dossier Éléments supprimés de la boutique principale. Les éléments marqués comme privés ne sont pas affichés. Les brouillons sont stockés dans le dossier Brouillons de la boutique principale. 
  
Cette propriété est ignorée si la version de Outlook est antérieure à Microsoft Office Outlook 2003 Service Pack 1, ou si sa valeur est **false**.
  

