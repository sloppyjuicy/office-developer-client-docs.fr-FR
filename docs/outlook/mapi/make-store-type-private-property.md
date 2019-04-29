---
title: Définir le type de magasin propriété privée
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Make Store Type Private Property
api_type:
- COM
ms.assetid: 7f489f55-46d4-8a88-6ebe-9db6446e69a5
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: da55afcabb1354959a71d6f10472c05540427b19
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428542"
---
# <a name="make-store-type-private-property"></a>Définir le type de magasin propriété privée

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Traite un magasin secondaire comme privé.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Exposé sur:  <br/> |[IMsgStore: objet IMAPIProp](imsgstoreimapiprop.md)  <br/> |
|Créé par:  <br/> |Fournisseur de magasin  <br/> |
|Accès par:  <br/> |Outlook et d'autres clients  <br/> |
|Type de propriété:  <br/> |PT_BOOLEAN  <br/> |
|Type d'accès:  <br/> |Lecture/écriture  <br/> |
   
## <a name="remarks"></a>Remarques

Pour fournir l'une des fonctionnalités de magasin, le fournisseur de banque doit implémenter [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) et renvoyer une balise de propriété valide pour l'une des propriétés transmises à un appel [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) . Lorsque la balise de propriété de l'une de ces propriétés est transmise à [IMAPIProp:: GetProps](imapiprop-getprops.md), le fournisseur Store doit également renvoyer la valeur de propriété correcte. Les fournisseurs de magasins peuvent appeler [HrGetOneProp](hrgetoneprop.md) et [HrSetOneProp](hrsetoneprop.md) pour obtenir ou définir ces propriétés. 
  
Pour récupérer la valeur de cette propriété, le client doit d'abord utiliser [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété, puis spécifier cette balise de propriété dans [IMAPIProp:: GetProps](imapiprop-getprops.md) pour obtenir la valeur. Lors de l'appel de [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md), spécifiez les valeurs suivantes pour la structure [MAPINAMEID](mapinameid.md) pointée par le paramètre d'entrée _lppPropNames_:
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind. lpwstrName:  <br/> |L "urn: schemas-microsoft-com: Office: Outlook # storetypeprivate"  <br/> |
   
Un fournisseur de banque peut utiliser cette propriété pour qu'Outlook le traite comme étant privé lorsqu'il s'agit d'une banque secondaire pour un utilisateur. 
  
Par défaut, Outlook traite une banque secondaire de la même manière qu'un magasin de délégués, et les éléments de la Banque secondaire ne sont privés que si l'utilisateur les marque spécifiquement comme étant privés. Lorsque cette propriété a la **valeur true**, les éléments supprimés d'une banque secondaire sont déplacés vers le dossier **éléments supprimés** dans le magasin principal. Les éléments marqués comme privés ne sont pas affichés. Les brouillons sont stockés dans le dossier Brouillons dans le magasin principal. 
  
Cette propriété est ignorée si la version d'Outlook est antérieure à Microsoft Office Outlook 2003 Service Pack 1, ou si sa valeur **** est false.
  

