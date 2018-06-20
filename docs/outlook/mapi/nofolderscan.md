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
ms.openlocfilehash: 3477104cc254ea5f22158b9791d7fd3bd776d819
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784906"
---
# <a name="nofolderscan"></a>NoFolderScan

  
  
**S’applique à**: Outlook 
  
Spécifie si Microsoft Office Outlook doit analyser les dossiers sur un magasin de Contacts.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Exposée sur :  <br/> |[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) objet  <br/> |
|Créé par :  <br/> |Fournisseur de banque  <br/> |
|Accessible par :  <br/> |Outlook et autres clients  <br/> |
|Type de propriété :  <br/> |PT_LONG  <br/> |
|Type d’accès :  <br/> |En lecture seule ou en lecture/écriture, selon le fournisseur de banque  <br/> |
   
## <a name="remarks"></a>Remarques

Pour fournir une des fonctionnalités de magasin, le fournisseur de banque doit implémenter [IMAPIProp : IUnknown](imapipropiunknown.md) et renvoyer une balise de propriété valide pour une de ces propriétés passées à un appel [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . Lorsque la balise de propriété pour une de ces propriétés est transmise à [IMAPIProp::GetProps](imapiprop-getprops.md), le fournisseur de banque doit également retourner la valeur de la propriété adéquate. Fournisseurs de magasins peuvent appeler [HrGetOneProp](hrgetoneprop.md) et [HrSetOneProp](hrsetoneprop.md) pour obtenir ou définir ces propriétés. 
  
Pour récupérer la valeur de cette propriété, le client doit d’abord utiliser [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété, puis spécifiez cette balise de propriété dans [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la valeur. Lors de l’appel [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), spécifiez les valeurs suivantes pour la structure [MAPINAMEID](mapinameid.md) sur laquelle pointé le paramètre d’entrée _lppPropNames_:
  
|||
|:-----|:-----|
|lpGuid :  <br/> |PSETID_Common  <br/> |
|ulKind :  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName :  <br/> |L « NoFolderScan »  <br/> |
   
Cette propriété permet de pour les fournisseurs de banque indiquer à Outlook ne pas analyser les dossiers de Contacts dans le magasin afin d’éviter une dégradation des performances. Il est utilisé dans les opérations de fusion et publipostage au cours de laquelle Outlook vérifie la présence et la valeur de cette propriété avant de lancer l’analyse.
  
Par défaut, cette propriété n’est pas exposée dans une banque, ce qui signifie qu’Outlook peut analyser le dossier Contacts dans le magasin. Si la propriété est exposée, les valeurs possibles sont les éléments suivants :
  
- Zéro (0) : Outlook peut effectuer l’analyse.
    
- Valeur non nulle : Outlook n’a pas doit analyser les dossiers sur le magasin de Contacts.
    

