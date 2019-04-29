---
title: IAddrBookDetails
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Details
api_type:
- COM
ms.assetid: 4eee4382-98c3-4714-8920-8d72edef00b8
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5fbd20a6b5d5598b8fa51f9c369eefac9a1ea2e9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424678"
---
# <a name="iaddrbookdetails"></a>IAddrBook::Details

  
  
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
  
> dans Pointeur vers un handle de la fenêtre parente de la boîte de dialogue.
    
 _lpfnDismiss_
  
> dans Pointeur vers une fonction basée sur le prototype [DISMISSMODELESS](dismissmodeless.md) , ou valeur null. Ce membre s'applique uniquement à la version non modale de la boîte de dialogue, comme indiqué par l'indicateur DIALOG_SDI défini. MAPI appelle la fonction **DISMISSMODELESS** lorsque l'utilisateur fait disparaître la boîte de dialogue d'adresses non modale, en informant un client qui appelle les **Détails** que la boîte de dialogue n'est plus active. 
    
 _lpvDismissContext_
  
> dans Pointeur vers les informations de contexte à transmettre à la fonction **DISMISSMODELESS** vers laquelle pointe le paramètre _lpfnDismiss_ . Ce paramètre s'applique uniquement à la version non modale de la boîte de dialogue, en incluant l'indicateur DIALOG_SDI dans le paramètre _ulFlags_ . 
    
 _cbEntryID_
  
> dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> dans Pointeur vers l'identificateur d'entrée pour l'entrée pour laquelle les détails sont affichés.
    
 _lpfButtonCallback_
  
> dans Pointeur vers une fonction basée sur le prototype de fonction [LPFNBUTTON](lpfnbutton.md) . Une fonction **LPFNBUTTON** ajoute un bouton à la boîte de dialogue détails. 
    
 _lpvButtonContext_
  
> dans Pointeur vers les données qui ont été utilisées comme paramètre pour la fonction spécifiée par le paramètre _lpfButtonCallback_ . 
    
 _lpszButtonText_
  
> dans Pointeur vers une chaîne qui contient le texte à appliquer au bouton ajouté, si ce bouton est extensible. Le paramètre _lpszButtonText_ doit être null si vous n'avez pas besoin d'un bouton extensible. 
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le type de texte pour le paramètre _lpszButtonText_ . Les indicateurs suivants peuvent être définis: 
    
AB_TELL_DETAILS_CHANGE
  
> Indique que les **Détails** renvoient la valeur S_OK si les modifications sont réellement apportées à l'adresse; dans le **** cas contraire, Details renvoie S_FALSE. 
    
DIALOG_MODAL
  
> Affiche la version modale de la boîte de dialogue adresse commune, qui s'affiche toujours dans les clients autres que Outlook. Cet indicateur est mutuellement exclusif avec DIALOG_SDI.
    
DIALOG_SDI
  
>  Affiche la version non modale de la boîte de dialogue adresse commune. Cet indicateur est ignoré pour les clients non-Outlook. 
    
MAPI_UNICODE 
  
> Les chaînes transmises sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La boîte de dialogue détails a été affichée pour l'entrée de carnet d'adresses.
    
## <a name="remarks"></a>Remarques

Les applications clientes **** appellent la méthode Details pour afficher une boîte de dialogue qui fournit des détails sur une entrée particulière dans le carnet d'adresses. Vous pouvez utiliser les paramètres _lpfButtonCallback_, _lpvButtonContext_et _lpszButtonText_ pour ajouter un bouton défini par le client à la boîte de dialogue. Lorsque l'utilisateur clique sur le bouton, MAPI appelle la fonction de rappel pointée par _lpfButtonCallback_, en transmettant l'identificateur d'entrée du bouton et les données dans _lpvButtonContext_. Si vous n'avez pas besoin d'un bouton extensible, _lpszButtonText_ doit être null. 
  
 Les **Détails** prennent en charge les chaînes de caractères Unicode; Les chaînes Unicode sont converties au format MBCS (Multibyte Character String) avant d'être affichées dans la boîte de dialogue détails. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|BaseDialog. cpp  <br/> |CBaseDialog:: OnOpenEntryID  <br/> |MFCMAPI utilise la **** méthode Details pour afficher une boîte de dialogue qui affiche les détails d'une entrée de carnet d'adresses.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[ADRPARM](adrparm.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

