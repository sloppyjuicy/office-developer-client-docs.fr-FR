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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 9923813d821e2b34497e3b498c19ce22ceda2eb0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783974"
---
# <a name="imapisupportdetails"></a>IMAPISupport::Details

  
  
**S’applique à**: Outlook 
  
Affiche une boîte de dialogue qui affiche des informations sur une entrée de carnet d’adresses particulière.
  
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

## <a name="parameters"></a>Paramètres

 _lpulUIParam_
  
> [out] Pointeur vers le handle vers la fenêtre parent de la boîte de dialogue renvoyée.
    
 _lpfnDismiss_
  
> [in] Pointeur vers une fonction basée sur le prototype [DISMISSMODELESS](dismissmodeless.md) ou NULL. Ce membre s’applique uniquement à la version de la boîte de dialogue non modale, telle qu’indiquée par l’indicateur DIALOG_SDI en cours. MAPI appelle la fonction **DISMISSMODELESS** lorsque l’utilisateur ferme la boîte de dialogue non modale adresse informant le client qui appelle **IMAPISupport::Details** que la boîte de dialogue n’est plus active. 
    
 _lpvDismissContext_
  
> [in] Un pointeur vers les informations de contexte à transmettre à la fonction **DISMISSMODELESS** indiqué par le paramètre _lpfnDismiss_ . Ce paramètre s’applique uniquement à la version de la boîte de dialogue non modale en incluant l’indicateur DIALOG_SDI dans le paramètre _ulFlags_ . 
    
 _cbEntryID_
  
> [in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée pour lesquels les détails sont affichés.
    
 _lpfButtonCallback_
  
> [in] Pointeur vers une fonction basée sur le prototype de fonction [LPFNBUTTON](lpfnbutton.md) . Une fonction **LPFNBUTTON** ajoute un bouton à la boîte de dialogue Détails. 
    
 _lpvButtonContext_
  
> [in] Pointeur vers les données utilisées en tant que paramètre pour la fonction spécifiée par le paramètre _lpfButtonCallback_ . 
    
 _lpszButtonText_
  
> [in] Pointeur vers une chaîne qui contient du texte peut être appliqué au bouton Ajout si ce bouton est extensible. Le paramètre _lpszButtonText_ doit être NULL si un bouton extensible n’est pas nécessaire. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type du texte pour le paramètre _lpszButtonText_ . Vous pouvez définir l’indicateur suivant : 
    
DIALOG_MODAL
  
> Afficher la version de la boîte de dialogue adresse modale. Cet indicateur est mutuellement exclusif avec DIALOG_SDI.
    
DIALOG_SDI
  
>  Afficher la version de la boîte de dialogue adresse non modale. Cet indicateur est mutuellement exclusif avec DIALOG_MODAL. 
    
MAPI_UNICODE 
  
> Les chaînes passée sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La boîte de dialogue a été correctement affichée pour l’entrée du carnet d’adresses.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::Details** est implémentée pour les objets de prise en charge du fournisseur adresse téléchargeable. Fournisseurs de carnet d’adresses appeler **Détails** pour afficher une boîte de dialogue qui donne des détails sur une entrée particulière dans le carnet d’adresses. Les paramètres _lpfButtonCallback_, _lpvButtonContext_et _lpszButtonText_ peuvent être utilisés pour ajouter un bouton défini par le client à la boîte de dialogue. Lorsque le bouton est activé, MAPI appelle la fonction de rappel désignée par _lpfButtonCallback_, en passant l’identificateur de l’entrée du bouton et les données _lpvButtonContext_. Si un bouton extensible n’est pas nécessaire, _lpszButtonText_ doit être NULL. 
  
## <a name="see-also"></a>Voir aussi



[ADRPARM](adrparm.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

