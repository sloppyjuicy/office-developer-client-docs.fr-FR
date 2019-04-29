---
title: CALLERRELEASE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CALLERRELEASE
api_type:
- HeaderDef
ms.assetid: 80ba893d-3380-4db1-9175-f5b84cb57def
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9a22550e60c9de38236a9f612c7e60f50f18978f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408725"
---
# <a name="callerrelease"></a>CALLERRELEASE

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit une fonction de rappel qui peut publier un objet de données de tableau lors de la publication d'un affichage de tableau. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
|Fonction définie implémentée par:  <br/> |Applications clientes et fournisseurs de services  <br/> |
|Fonction définie appelée par:  <br/> |MAPI  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a>Paramètres

 _ulCallerData_
  
> dans Données de l'appelant enregistrées par MAPI avec la vue de table et transmises à la fonction de rappel basée sur **CALLERRELEASE** . Les données fournissent un contexte sur l'affichage tableau en cours de publication. 
    
 _lpTblData_
  
> dans Pointeur vers l'interface [ITableData: IUnknown](itabledataiunknown.md) pour l'objet de données de tableau sous-jacent de la vue de tableau en cours de publication. 
    
 _lpVue_
  
> dans Pointeur vers l'interface [IMAPITable: IUnknown](imapitableiunknown.md) pour l'affichage tableau en cours de publication. Il s'agit d'une interface pour l'objet Table renvoyé dans le paramètre _lppMAPITable_ de la méthode [ITableData:: HrGetView](itabledata-hrgetview.md) qui a créé l'objet à libérer. 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun 
  
## <a name="remarks"></a>Remarques

Une application cliente ou un fournisseur de services qui a rempli un objet de données de table peut appeler [ITableData:: HrGetView](itabledata-hrgetview.md) pour créer une vue triée en lecture seule de la table. L'appel à **HrGetView** transmet un pointeur vers une fonction de rappel basée sur **CALLERRELEASE** et également un contexte à enregistrer avec la vue de table. Lorsque le décompte de références de l'affichage de tableau est remis à zéro et que la vue est publiée, l'implémentation de la méthode **IMAPITable** appelle la fonction de rappel, en transmettant le contexte dans le paramètre _ulCallerData_ . 
  
Une utilisation courante d'une fonction de rappel basée sur **CALLERRELEASE** consiste à libérer l'objet de données de la table sous-jacente et à ne pas le suivre pendant un traitement ultérieur. 
  

