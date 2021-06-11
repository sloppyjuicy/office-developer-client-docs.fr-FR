---
title: IMAPISupportDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Details
api_type:
- COM
ms.assetid: 1a62efa2-dd6b-4acb-a760-defa601c20c9
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: bdc57a6e951e54640fe3c638977c6a5f16986e68
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426778"
---
# <a name="imapisupportdetails"></a>IMAPISupport::Details

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Affiche une boîte de dialogue qui affiche des détails sur une entrée de carnet d’adresses particulière.
  
```cpp
HRESULT Details(
  ULONG_PTR FAR * lpulUIParam,
  LPFNDISMISS lpfnDismiss,
  LPVOID lpvDismissContext,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPFNBUTTON lpfButtonCallback,
  LPVOID lpvButtonContext,
  LPSTR lpszButtonText,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpulUIParam_
  
> [out] Pointeur vers la poignée vers la fenêtre parente de la boîte de dialogue renvoyée.
    
 _lpfnDismiss_
  
> [in] Pointeur vers une fonction basée sur le prototype [DISMISSMODELESS](dismissmodeless.md) ou NULL. Ce membre s’applique uniquement à la version sans mode de la boîte de dialogue, comme indiqué par l’indicateur DIALOG_SDI en cours de mise en place. MAPI appelle la fonction **DISMISSMODELESS** lorsque l’utilisateur fait disparaître la boîte de dialogue d’adresses sans mode, informant un client qui appelle **IMAPISupport::D etails** que la boîte de dialogue n’est plus active. 
    
 _lpvDismissContext_
  
> [in] Pointeur vers les informations de contexte à transmettre à la **fonction DISMISSMODELESS** pointée par le paramètre _lpfnDismiss._ Ce paramètre s’applique uniquement à la version sans mode de la boîte de dialogue, en incluant l’indicateur DIALOG_SDI dans le _paramètre ulFlags._ 
    
 _cbEntryID_
  
> [in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpEntryID._ 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée pour lequel les détails sont affichés.
    
 _lpfButtonCallback_
  
> [in] Pointeur vers une fonction basée sur le prototype de fonction [LPFNBUTTON.](lpfnbutton.md) Une **fonction LPFNBUTTON** ajoute un bouton à la boîte de dialogue Détails. 
    
 _lpvButtonContext_
  
> [in] Pointeur vers des données utilisées comme paramètre pour la fonction spécifiée par le paramètre _lpfButtonCallback._ 
    
 _lpszButtonText_
  
> [in] Pointeur vers une chaîne qui contient du texte à appliquer au bouton ajouté si ce bouton est extensible. Le  _paramètre lpszButtonText_ doit être NULL si un bouton extensible n’est pas nécessaire. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type du texte pour le _paramètre lpszButtonText._ L’indicateur suivant peut être définie : 
    
DIALOG_MODAL
  
> Affiche la version modale de la boîte de dialogue d’adresse commune. Cet indicateur s’exclue mutuellement avec DIALOG_SDI.
    
DIALOG_SDI
  
>  Affiche la version non modée de la boîte de dialogue d’adresse commune. Cet indicateur s’exclue mutuellement avec DIALOG_MODAL. 
    
MAPI_UNICODE 
  
> Les chaînes transmises sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La boîte de dialogue Détails a été affichée avec succès pour l’entrée du carnet d’adresses.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISupport::D etails** est implémentée pour les objets de prise en charge du fournisseur de carnet d’adresses. Les fournisseurs de carnets d’adresses appellent **Details** pour afficher une boîte de dialogue qui fournit des détails sur une entrée particulière dans le carnet d’adresses. Les  _paramètres lpfButtonCallback,_  _lpvButtonContext_ et  _lpszButtonText_ peuvent être utilisés pour ajouter un bouton défini par le client à la boîte de dialogue. Lorsque vous cliquez sur le bouton, MAPI appelle la fonction de rappel pointée par  _lpfButtonCallback_, en passant l’identificateur d’entrée du bouton et les données dans  _lpvButtonContext_. Si un bouton extensible n’est pas nécessaire,  _lpszButtonText_ doit être NULL. 
  
## <a name="see-also"></a>Voir aussi



[ADRPARM](adrparm.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

