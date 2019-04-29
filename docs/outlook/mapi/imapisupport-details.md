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
  
Affiche une boîte de dialogue qui affiche des détails sur une entrée de carnet d'adresses particulière.
  
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
  
> remarquer Pointeur vers le handle de la fenêtre parente de la boîte de dialogue renvoyée.
    
 _lpfnDismiss_
  
> dans Pointeur vers une fonction basée sur le prototype [DISMISSMODELESS](dismissmodeless.md) , ou valeur null. Ce membre s'applique uniquement à la version non modale de la boîte de dialogue, comme indiqué par l'indicateur DIALOG_SDI défini. MAPI appelle la fonction **DISMISSMODELESS** lorsque l'utilisateur fait disparaître la boîte de dialogue d'adresses non modale, en informant un client qui appelle **IMAPISupport::D etails** que la boîte de dialogue n'est plus active. 
    
 _lpvDismissContext_
  
> dans Pointeur vers les informations de contexte à transmettre à la fonction **DISMISSMODELESS** vers laquelle pointe le paramètre _lpfnDismiss_ . Ce paramètre s'applique uniquement à la version non modale de la boîte de dialogue, en incluant l'indicateur DIALOG_SDI dans le paramètre _ulFlags_ . 
    
 _cbEntryID_
  
> dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> dans Pointeur vers l'identificateur d'entrée pour laquelle les détails sont affichés.
    
 _lpfButtonCallback_
  
> dans Pointeur vers une fonction basée sur le prototype de fonction [LPFNBUTTON](lpfnbutton.md) . Une fonction **LPFNBUTTON** ajoute un bouton à la boîte de dialogue détails. 
    
 _lpvButtonContext_
  
> dans Pointeur vers les données utilisées comme paramètre pour la fonction spécifiée par le paramètre _lpfButtonCallback_ . 
    
 _lpszButtonText_
  
> dans Pointeur vers une chaîne qui contient le texte à appliquer au bouton ajouté si ce bouton est extensible. Le paramètre _lpszButtonText_ doit être null si aucun bouton extensible n'est nécessaire. 
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le type de texte pour le paramètre _lpszButtonText_ . L'indicateur suivant peut être défini: 
    
DIALOG_MODAL
  
> Affiche la version modale de la boîte de dialogue adresse commune. Cet indicateur est mutuellement exclusif avec DIALOG_SDI.
    
DIALOG_SDI
  
>  Affiche la version non modale de la boîte de dialogue adresse commune. Cet indicateur est mutuellement exclusif avec DIALOG_MODAL. 
    
MAPI_UNICODE 
  
> Les chaînes transmises sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La boîte de dialogue détails a été affichée pour l'entrée de carnet d'adresses.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::D etails** est implémentée pour les objets de prise en charge du fournisseur de carnets d'adresses. Fournisseurs de carnet d'adresses **Détails** des appels pour afficher une boîte de dialogue qui fournit des détails sur une entrée particulière dans le carnet d'adresses. Les paramètres _lpfButtonCallback_, _lpvButtonContext_et _lpszButtonText_ peuvent être utilisés pour ajouter un bouton défini par le client à la boîte de dialogue. Lorsque l'utilisateur clique sur le bouton, MAPI appelle la fonction de rappel pointée par _lpfButtonCallback_, en transmettant l'identificateur d'entrée du bouton et les données dans _lpvButtonContext_. Si un bouton extensible n'est pas nécessaire, _lpszButtonText_ doit être null. 
  
## <a name="see-also"></a>Voir aussi



[ADRPARM](adrparm.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

