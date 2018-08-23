---
title: Propriété de privatisation du type de magasin
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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 2d927b00391725d8804e41b66b1ec8c384f98e7c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568832"
---
# <a name="make-store-type-private-property"></a>Propriété de privatisation du type de magasin

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Traite un stockage secondaire comme privée.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Exposée sur :  <br/> |[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) objet  <br/> |
|Créé par :  <br/> |Fournisseur de banque  <br/> |
|Accessible par :  <br/> |Outlook et autres clients  <br/> |
|Type de propriété :  <br/> |PT_BOOLEAN  <br/> |
|Type d’accès :  <br/> |En lecture-écriture.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour fournir une des fonctionnalités de magasin, le fournisseur de banque doit implémenter [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) et renvoyer une balise de propriété valide pour une de ces propriétés passées à un appel [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . Lorsque la balise de propriété pour une de ces propriétés est transmise à [IMAPIProp::GetProps](imapiprop-getprops.md), le fournisseur de banque doit également retourner la valeur de la propriété adéquate. Fournisseurs de magasins peuvent appeler [HrGetOneProp](hrgetoneprop.md) et [HrSetOneProp](hrsetoneprop.md) pour obtenir ou définir ces propriétés. 
  
Pour récupérer la valeur de cette propriété, le client doit d’abord utiliser [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété, puis spécifiez cette balise de propriété dans [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la valeur. Lors de l’appel [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), spécifiez les valeurs suivantes pour la structure [MAPINAMEID](mapinameid.md) sur laquelle pointé le paramètre d’entrée _lppPropNames_:
  
|||
|:-----|:-----|
|lpGuid :  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulKind :  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName :  <br/> |L « urn : schemas-microsoft-com:office:outlook #storetypeprivate »  <br/> |
   
Un fournisseur de magasin de cette propriété permet à Outlook de traiter comme privée lorsqu’il s’agit d’un magasin secondaire pour un utilisateur. 
  
Par défaut, Outlook traite un stockage secondaire de la même manière comme une banque déléguée et éléments dans le magasin secondaire sont privés uniquement si l’utilisateur les marque spécifiquement comme étant privé. Lorsque cette propriété a la **valeur true**, les éléments supprimés à partir d’un stockage secondaire sont déplacés vers le dossier **Éléments supprimés** dans le magasin principal. Éléments marqués comme privés ne sont pas affichées. Brouillons sont stockés dans le dossier Brouillons dans le magasin principal. 
  
Cette propriété est ignorée si la version d’Outlook est antérieure à Microsoft Office Outlook 2003 Service Pack 1, ou si sa valeur est **false**.
  

