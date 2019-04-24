---
title: NoFolderScan
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4949aef9-4c96-82cc-cd13-57981e07cc40
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: fc5f5a42e2b1e57374ff80a9333b927cc8dba120
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326263"
---
# <a name="nofolderscan"></a>NoFolderScan

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique si Microsoft Office Outlook doit analyser les dossiers de contacts d'une banque d'information.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Exposé sur:  <br/> |[IMsgStore: objet IMAPIProp](imsgstoreimapiprop.md)  <br/> |
|Créé par:  <br/> |Fournisseur de magasin  <br/> |
|Accès par:  <br/> |Outlook et d'autres clients  <br/> |
|Type de propriété:  <br/> |PT_LONG  <br/> |
|Type d'accès:  <br/> |Lecture seule ou lecture/écriture en fonction du fournisseur de la Banque  <br/> |
   
## <a name="remarks"></a>Remarques

Pour fournir l'une des fonctionnalités de magasin, le fournisseur de banque doit implémenter [IMAPIProp: IUnknown](imapipropiunknown.md) et renvoyer une balise de propriété valide pour l'une des propriétés transmises à un appel [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) . Lorsque la balise de propriété de l'une de ces propriétés est transmise à [IMAPIProp:: GetProps](imapiprop-getprops.md), le fournisseur Store doit également renvoyer la valeur de propriété correcte. Les fournisseurs de magasins peuvent appeler [HrGetOneProp](hrgetoneprop.md) et [HrSetOneProp](hrsetoneprop.md) pour obtenir ou définir ces propriétés. 
  
Pour récupérer la valeur de cette propriété, le client doit d'abord utiliser [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété, puis spécifier cette balise de propriété dans [IMAPIProp:: GetProps](imapiprop-getprops.md) pour obtenir la valeur. Lors de l'appel de [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md), spécifiez les valeurs suivantes pour la structure [MAPINAMEID](mapinameid.md) pointée par le paramètre d'entrée _lppPropNames_:
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind. lpwstrName:  <br/> |L "NoFolderScan"  <br/> |
   
Cette propriété permet aux fournisseurs de magasin de spécifier à Outlook de ne pas analyser les dossiers de contacts dans le magasin pour éviter une dégradation des performances. Elle est utilisée dans les opérations de fusion et publipostage au cours desquelles Outlook vérifie la présence et la valeur de cette propriété avant de lancer l'analyse.
  
Par défaut, cette propriété n'est pas exposée sur un magasin, ce qui signifie qu'Outlook peut analyser le dossier contacts de la Banque. Si la propriété est exposée, les valeurs possibles sont les suivantes:
  
- Zéro (0): Outlook peut effectuer l'analyse.
    
- Valeur non nulle: Outlook ne doit pas analyser les dossiers de contacts de la Banque.
    

