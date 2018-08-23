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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 32174e213334d784220b960364443e60db6d1d19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582776"
---
# <a name="imapisupportdoprogressdialog"></a>IMAPISupport::DoProgressDialog

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
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
  
> [in] Un handle vers la fenêtre parent de l’indicateur de progression.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle comment l’objet de l’avancement doit calculer l’avancement. Vous pouvez définir l’indicateur suivant :
    
MAPI_TOP_LEVEL 
  
> Progression est calculée pour un élément de niveau supérieur, par exemple un dossier parent. L’objet de l’avancement doit utiliser les valeurs dans la méthode [IMAPIProgress::Progress](imapiprogress-progress.md) _ulCount_ et _ulTotal_ — qui indiquent l’élément actuel et le nombre total d’éléments dans l’opération, respectivement, pour incrémenter la progression indicateur de l’opération. 
    
 _lppProgress_
  
> [out] Pointeur vers un pointeur vers l’objet de progression.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La progression de l’objet a été extrait.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::DoProgressDialog** est implémentée pour adresse livre et message fournisseur prise en charge des objets store. Ces fournisseurs appellent **DoProgressDialog** pour accéder à l’implémentation de l’interface [IMAPIProgress](imapiprogressiunknown.md) , qui calcule les informations de progression et affiche une boîte de dialogue standard MAPI. 
  
Pour plus d’informations sur l’utilisation d’un objet de progression et l’interface **IMAPIProgress** , voir [Afficher un indicateur de progression](how-to-display-a-progress-indicator.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)


[Afficher un indicateur de progression](how-to-display-a-progress-indicator.md)

