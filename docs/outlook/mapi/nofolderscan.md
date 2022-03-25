---
title: NoFolderScan
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 4949aef9-4c96-82cc-cd13-57981e07cc40
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4fae7cd160020b11e96f674cd8941b35c1da7ff1
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63782040"
---
# <a name="nofolderscan"></a>NoFolderScan

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie si Microsoft Office Outlook doit analyser les dossiers Contacts d’une boutique.
  
## <a name="quick-info"></a>Informations rapides

|Propriété|Valeur|
|:-----|:-----|
|Exposé sur :  <br/> |[IMsgStore : objet IMAPIProp](imsgstoreimapiprop.md)  <br/> |
|Créé par :  <br/> |Fournisseur du Store  <br/> |
|Accessible par :  <br/> |Outlook clients et autres clients  <br/> |
|Type de propriété :  <br/> |PT_LONG  <br/> |
|Type d’accès :  <br/> |En lecture seule ou en lecture/écriture en fonction du fournisseur du magasin  <br/> |
   
## <a name="remarks"></a>Remarques

Pour fournir l’une des fonctionnalités du magasin, le fournisseur de magasin doit implémenter [IMAPIProp : IUnknown](imapipropiunknown.md) et renvoyer une balise de propriété valide pour l’une de ces propriétés transmises à un appel [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . Lorsque la balise de propriété de l’une de ces propriétés est transmise à [IMAPIProp::GetProps](imapiprop-getprops.md), le fournisseur de magasins doit également renvoyer la valeur de propriété correcte. Les fournisseurs du Store peuvent appeler [HrGetOneProp](hrgetoneprop.md) et [HrSetOneProp](hrsetoneprop.md) pour obtenir ou définir ces propriétés. 
  
Pour récupérer la valeur de cette propriété, le client doit d’abord utiliser [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété, puis spécifier cette balise de propriété dans [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la valeur. Lorsque vous appelez [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), spécifiez les valeurs suivantes pour la structure [MAPINAMEID](mapinameid.md) pointée par le paramètre d’entrée  _lppPropNames_ :
  
|Propriété|Valeur|
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind :  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName :  <br/> |L"NoFolderScan »  <br/> |
   
Cette propriété permet aux fournisseurs de magasins de spécifier Outlook ne pas analyser les dossiers contacts de la boutique afin d’éviter la dégradation des performances. Il est utilisé dans les opérations de fusion et publipostage au cours des Outlook la présence et la valeur de cette propriété avant de lancer l’analyse.
  
Par défaut, cette propriété n’est pas exposée dans une boutique, ce qui signifie Outlook peut analyser le dossier Contacts de la boutique. Si la propriété est exposée, les valeurs possibles sont les suivantes :
  
- Zéro (0) : Outlook pouvez effectuer l’analyse.
    
- Valeur non nulle : Outlook ne doit pas analyser les dossiers Contacts de la boutique.
    

