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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 69ee06ef8c8f5499dec41232d3dc7b374b15a744
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782993"
---
# <a name="callerrelease"></a>CALLERRELEASE

  
  
**S’applique à**: Outlook 
  
Définit une fonction de rappel pouvant déclencher un objet de données de table lors de l’affichage tableau a été publié. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Fonction implémentée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
|Fonction appelée par :  <br/> |MAPI  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a>Paramètres

 _ulCallerData_
  
> [in] Fonction de rappel en fonction de données de l’appelant enregistré par MAPI avec l’affichage tableau et transmises à la **CALLERRELEASE** . Les données fournissent un contexte relatif à l’affichage tableau libéré. 
    
 _lpTblData_
  
> [in] Pointeur vers le [ITableData : IUnknown](itabledataiunknown.md) interface pour l’objet de données de table sous-jacentes de la vue table publiée. 
    
 _lpVue_
  
> [in] Pointeur vers le [IMAPITable : IUnknown](imapitableiunknown.md) interface pour l’affichage de la table publiée. Il s’agit d’une interface de l’objet table renvoyé dans le paramètre _lppMAPITable_ de la méthode [ITableData::HrGetView](itabledata-hrgetview.md) qui a créé l’objet pour libérer. 
    
## <a name="return-value"></a>Valeur renvoy�e

Aucune 
  
## <a name="remarks"></a>Remarques

Une application cliente ou un fournisseur de services qui a rempli un objet de données de table peut appeler [ITableData::HrGetView](itabledata-hrgetview.md) pour créer un affichage en lecture seule, trié de la table. L’appel vers **HrGetView** passe un pointeur vers une fonction de rappel **CALLERRELEASE** basé et également un contexte soit enregistré avec l’affichage tableau. Lorsque le décompte de références de l’affichage tableau renvoie zéro et la vue est publiée, l’implémentation **IMAPITable** appelle la fonction de rappel, en passant le contexte dans le paramètre _ulCallerData_ . 
  
Une utilisation courante d’une fonction de rappel **CALLERRELEASE** en est pour libérer de l’objet de données de table sous-jacente et n’ont pas à garder une trace des il lors du traitement suivant. 
  

