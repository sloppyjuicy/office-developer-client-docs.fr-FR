---
title: IMAPIControlActivate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.Activate
api_type:
- COM
ms.assetid: 2b641030-2429-4217-a648-0a9f3d1a1b29
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: d3b47e423daf428c67761d13deef1ae0858c91c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280201"
---
# <a name="imapicontrolactivate"></a>IMAPIControl::Activate

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Effectue une tâche telle que l'affichage d'une boîte de dialogue ou le lancement d'une opération par programme lorsqu'un utilisateur d'application cliente clique sur le contrôle de bouton.
  
```cpp
HRESULT Activate(
  ULONG ulFlags,
  ULONG_PTR ulUIParam
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _ulUIParam_
  
> dans Handle de la fenêtre parent de la boîte de dialogue dans laquelle apparaît le contrôle de bouton.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le contrôle bouton a été activé avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIControl:: Activate** effectue les tâches qui suivent le clic d'un utilisateur sur le contrôle Button. Une fois que le clic se produit, dans le cadre du traitement de la table d'affichage, MAPI appelle l' **activation** après le premier appel de [IMAPIControl:: GetState](imapicontrol-getstate.md) pour déterminer si le bouton est activé. 
  
Pour plus d'informations sur l'implémentation de l' **activation** et sur les autres méthodes [IMAPIControl: IUnknown](imapicontroliunknown.md) , consultez la rubrique [Control Object Implementation](control-object-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPIControl::GetState](imapicontrol-getstate.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

