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
ms.openlocfilehash: 7f330ef3099175dde88bec2de3512a3c4af1db49
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580683"
---
# <a name="imapicontrolactivate"></a>IMAPIControl::Activate

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Effectue une tâche telle que l’affichage d’une boîte de dialogue ou le démarrage d’une opération de programmation lorsqu’un utilisateur de l’application client clique sur le contrôle bouton.
  
```cpp
HRESULT Activate(
  ULONG ulFlags,
  ULONG_PTR ulUIParam
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _ulUIParam_
  
> [in] Handle vers la fenêtre parente de la boîte de dialogue sur lequel apparaît le contrôle bouton.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le contrôle bouton a été activé avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIControl::Activate** effectue des tâches suivant un bouton du contrôle bouton. Une fois que le clic se produit dans le cadre du traitement de la table d’affichage, MAPI effectue un appel à **Activer** après le premier appel [IMAPIControl::GetState](imapicontrol-getstate.md) pour déterminer si le bouton est activé. 
  
Pour plus d’informations sur la façon d’implémenter **Activate** et l’autre [IMAPIControl : IUnknown](imapicontroliunknown.md) méthodes, voir [Implémentation d’objet de contrôle](control-object-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPIControl::GetState](imapicontrol-getstate.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

