---
title: CALLERRELEASE
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ad1f6408b7da14027c4b84d09575d06091381371
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567843"
---
# <a name="callerrelease"></a>CALLERRELEASE

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit une fonction de rappel qui peut libérer un objet de données de table lorsqu’une vue de table est relâchée. 
  
|||
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
  
> [in] Données de l’appelant enregistrées par MAPI avec l’affichage Table et transmises à la fonction de rappel basée sur **CALLERRELEASE.** Les données fournissent un contexte sur la vue de table en cours de publication. 
    
 _lpTblData_
  
> [in] Pointeur vers l’interface [ITableData : IUnknown](itabledataiunknown.md) pour l’objet de données de table sous-jacent à la vue de table publiée. 
    
 _lpVue_
  
> [in] Pointeur vers [l’interface IMAPITable : IUnknown](imapitableiunknown.md) pour la vue de table en cours de publication. Il s’agit d’une interface pour l’objet table renvoyé dans le paramètre  _lppMAPITable_ de la méthode [ITableData::HrGetView](itabledata-hrgetview.md) qui a créé l’objet à libérer. 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun 
  
## <a name="remarks"></a>Remarques

Une application cliente ou un fournisseur de services qui a rempli un objet de données de table peut appeler [ITableData::HrGetView](itabledata-hrgetview.md) pour créer une vue triée en lecture seule de la table. L’appel **à HrGetView** transmet un pointeur à une fonction de rappel basée sur **CALLERRELEASE,** ainsi qu’un contexte à enregistré avec l’affichage Tableau. Lorsque le nombre de références de l’affichage Table revient à zéro et que l’affichage est libéré, l’implémentation **IMAPITable** appelle la fonction de rappel, en passant le contexte dans le paramètre _ulCallerData._ 
  
Une utilisation courante d’une fonction de rappel basée sur **CALLERRELEASE** consiste à libérer l’objet de données de table sous-jacent et à ne pas avoir à le suivre lors du traitement ultérieur. 
  

