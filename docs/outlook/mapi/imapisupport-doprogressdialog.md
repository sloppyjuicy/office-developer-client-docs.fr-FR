---
title: IMAPISupportDoProgressDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.DoProgressDialog
api_type:
- COM
ms.assetid: 74c52b96-e903-444b-8bda-73a08f278c22
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2941178a46b6cd1323d3ccb8ffe3acd97f631155
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620890"
---
# <a name="imapisupportdoprogressdialog"></a>IMAPISupport::DoProgressDialog

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Récupère un objet de progression qui affiche un indicateur de progression.
  
```cpp
HRESULT DoProgressDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIPROGRESS FAR * lppProgress
);
```

## <a name="parameters"></a>Paramètres

 _ulUIParam_
  
> [in] Handle vers la fenêtre parent de l’indicateur de progression.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet de progression doit calculer la progression. L’indicateur suivant peut être définie :
    
MAPI_TOP_LEVEL 
  
> La progression est calculée pour un élément de niveau supérieur, tel qu’un dossier parent. L’objet de progression doit utiliser les valeurs des paramètres _ulCount_ et _ulTotal_ de la méthode [IMAPIProgress::P rogress](imapiprogress-progress.md) , qui indiquent respectivement l’élément actuel et le nombre total d’éléments de l’opération, pour incrémenter l’indicateur de progression de l’opération. 
    
 _lppProgress_
  
> [out] Pointeur vers un pointeur vers l’objet de progression.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’objet de progression a été récupéré avec succès.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISupport::D oProgressDialog** est implémentée pour les objets de prise en charge du carnet d’adresses et du fournisseur de magasins de messages. Ces fournisseurs **appellent DoProgressDialog** pour accéder à l’implémentation MAPI de l’interface [IMAPIProgress,](imapiprogressiunknown.md) qui calcule les informations de progression et affiche une boîte de dialogue standard. 
  
Pour plus d’informations sur l’utilisation d’un objet de progression et de l’interface **IMAPIProgress,** voir [Afficher un indicateur de progression.](how-to-display-a-progress-indicator.md)
  
## <a name="see-also"></a>Voir aussi



[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)


[Affichage d’un indicateur de progression](how-to-display-a-progress-indicator.md)

