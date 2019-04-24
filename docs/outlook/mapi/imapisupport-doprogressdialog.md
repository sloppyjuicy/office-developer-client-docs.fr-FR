---
title: IMAPISupportDoProgressDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoProgressDialog
api_type:
- COM
ms.assetid: 74c52b96-e903-444b-8bda-73a08f278c22
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 3de29e9af5caa82d2e57c8fcbbdab7d5ddb19dd9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285205"
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
  
> dans Handle de la fenêtre parent de l'indicateur de progression.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle la manière dont l'objet Progress doit calculer la progression. L'indicateur suivant peut être défini:
    
MAPI_TOP_LEVEL 
  
> La progression est calculée pour un élément de niveau supérieur, tel qu'un dossier parent. L'objet Progress doit utiliser les valeurs des paramètres _ulCount_ et _ulTotal_ de la méthode [méthode imapiprogress::P rogress](imapiprogress-progress.md) , qui indiquent respectivement l'élément actif et le nombre total d'éléments dans l'opération; pour incrémenter la progression indicateur de l'opération. 
    
 _lppProgress_
  
> remarquer Pointeur vers un pointeur vers l'objet de progression.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'objet Progress a été correctement récupéré.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::D oprogressdialog** est implémentée pour les objets de prise en charge des fournisseurs de banques de messages et de carnet d'adresses. Ces fournisseurs appellent **DoProgressDialog** pour accéder à l'implémentation MAPI de l'interface [méthode imapiprogress](imapiprogressiunknown.md) , qui calcule les informations d'avancement et affiche une boîte de dialogue standard. 
  
Pour plus d'informations sur l'utilisation d'un objet Progress et de l'interface **méthode imapiprogress** , voir [afficher un indicateur de progression](how-to-display-a-progress-indicator.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)


[Affichage d’un indicateur de progression](how-to-display-a-progress-indicator.md)

