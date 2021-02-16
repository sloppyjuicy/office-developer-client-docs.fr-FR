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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d3b47e423daf428c67761d13deef1ae0858c91c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418014"
---
# <a name="imapicontrolactivate"></a>IMAPIControl::Activate

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Effectue une tâche telle que l’affichage d’une boîte de dialogue ou le démarrage d’une opération par programme lorsqu’un utilisateur de l’application cliente clique sur le contrôle de bouton.
  
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
  
> [in] Poignée vers la fenêtre parente de la boîte de dialogue sur laquelle le contrôle de bouton apparaît.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le contrôle de bouton a été activé avec succès.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPIControl::Activate** effectue des tâches à la suite du clic d’un utilisateur sur le contrôle de bouton. Une fois que le clic s’est produit, dans le cadre du traitement de la table d’affichage, MAPI appelle **Activate** après avoir appelé [IMAPIControl::GetState](imapicontrol-getstate.md) pour déterminer si le bouton est activé. 
  
Pour plus d’informations sur l’implémentation **d’Activate** et des autres méthodes [IMAPIControl : IUnknown,](imapicontroliunknown.md) voir [Control Object Implementation](control-object-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPIControl::GetState](imapicontrol-getstate.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

