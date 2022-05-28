---
title: CALLERRELEASE
description: CALLERRELEASE définit une fonction de rappel qui peut libérer un objet de données de table lors de la publication d’une vue de table.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CALLERRELEASE
api_type:
- HeaderDef
ms.assetid: 80ba893d-3380-4db1-9175-f5b84cb57def
ms.openlocfilehash: 7df7fe628b95b1e30993b078f00b5a7a0d97609e
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65769871"
---
# <a name="callerrelease"></a>CALLERRELEASE

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit une fonction de rappel qui peut libérer un objet de données de table lors de la publication d’un affichage table. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Fonction définie implémentée par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
|Fonction définie appelée par :  <br/> |MAPI  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a>Paramètres

 _ulCallerData_
  
> [in] Données de l’appelant enregistrées par MAPI avec la vue table et transmises à la fonction de rappel basée sur **CALLERRELEASE** . Les données fournissent un contexte sur la vue de table en cours de publication. 
    
 _lpTblData_
  
> [in] Pointeur vers l’interface [ITableData : IUnknown](itabledataiunknown.md) pour l’objet de données de table sous-jacent à la vue table en cours de publication. 
    
 _lpVue_
  
> [in] Pointeur vers l’interface [IMAPITable : IUnknown](imapitableiunknown.md) pour la vue table en cours de publication. Il s’agit d’une interface pour l’objet table retourné dans le paramètre _lppMAPITable_ de la méthode [ITableData::HrGetView](itabledata-hrgetview.md) qui a créé l’objet à libérer. 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun 
  
## <a name="remarks"></a>Remarques

Une application cliente ou un fournisseur de services qui a rempli un objet de données de table peut appeler [ITableData::HrGetView](itabledata-hrgetview.md) pour créer une vue triée en lecture seule de la table. L’appel à **HrGetView** transmet un pointeur à une fonction de rappel **CALLERRELEASE** et un contexte à enregistrer avec la vue table. Lorsque le nombre de références de la vue de table revient à zéro et que la vue est en cours de publication, l’implémentation **IMAPITable** appelle la fonction de rappel, en passant le contexte dans le paramètre _ulCallerData_ . 
  
Une utilisation courante d’une fonction de rappel basée sur **CALLERRELEASE** consiste à libérer l’objet de données de table sous-jacent et à ne pas avoir à le suivre pendant le traitement suivant. 
  

