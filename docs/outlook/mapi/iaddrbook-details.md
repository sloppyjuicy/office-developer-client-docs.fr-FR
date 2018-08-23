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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: e240ec4e7a61b9e7484f467926501f8c5f5a59f8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592345"
---
# <a name="iaddrbookdetails"></a>IAddrBook::Details

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
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
  
> [in] Pointeur vers un handle de fenêtre parente de la boîte de dialogue.
    
 _lpfnDismiss_
  
> [in] Pointeur vers une fonction basée sur le prototype [DISMISSMODELESS](dismissmodeless.md) ou NULL. Ce membre s’applique uniquement à la version de la boîte de dialogue non modale, telle qu’indiquée par l’indicateur DIALOG_SDI en cours. MAPI appelle la fonction **DISMISSMODELESS** lorsque l’utilisateur ferme la boîte de dialogue non modale adresse informant le client qui appelle **plus d’informations** que la boîte de dialogue n’est plus active. 
    
 _lpvDismissContext_
  
> [in] Un pointeur vers les informations de contexte à transmettre à la fonction **DISMISSMODELESS** indiqué par le paramètre _lpfnDismiss_ . Ce paramètre s’applique uniquement à la version de la boîte de dialogue non modale en incluant l’indicateur DIALOG_SDI dans le paramètre _ulFlags_ . 
    
 _cbEntryID_
  
> [in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée pour l’entrée pour laquelle les détails sont affichés.
    
 _lpfButtonCallback_
  
> [in] Pointeur vers une fonction basée sur le prototype de fonction [LPFNBUTTON](lpfnbutton.md) . Une fonction **LPFNBUTTON** ajoute un bouton à la boîte de dialogue Détails. 
    
 _lpvButtonContext_
  
> [in] Pointeur vers les données qui a été utilisés en tant que paramètre pour la fonction spécifiée par le paramètre _lpfButtonCallback_ . 
    
 _lpszButtonText_
  
> [in] Pointeur vers une chaîne qui contient du texte à appliquer au bouton ajouté, si ce bouton est extensible. Le paramètre _lpszButtonText_ doit être NULL si vous n’avez pas besoin d’un bouton extensible. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type du texte pour le paramètre _lpszButtonText_ . Les indicateurs suivants peuvent être définis : 
    
AB_TELL_DETAILS_CHANGE
  
> Indique que **les détails** renvoie S_OK si les modifications sont réellement apportées à l’adresse ; dans le cas contraire, les **Détails** renvoie S_FALSE. 
    
DIALOG_MODAL
  
> Afficher la version de la boîte de dialogue adresse, qui est toujours affichée dans les clients Outlook-non modale. Cet indicateur est mutuellement exclusif avec DIALOG_SDI.
    
DIALOG_SDI
  
>  Afficher la version de la boîte de dialogue adresse non modale. Cet indicateur est ignoré pour les clients non Outlook. 
    
MAPI_UNICODE 
  
> Les chaînes passée sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La boîte de dialogue a été correctement affichée pour l’entrée du carnet d’adresses.
    
## <a name="remarks"></a>Remarques

Applications clientes appellent la méthode **Details** pour afficher une boîte de dialogue qui fournit des détails sur une entrée particulière dans le carnet d’adresses. Vous pouvez utiliser les paramètres _lpfButtonCallback_, _lpvButtonContext_et _lpszButtonText_ pour ajouter un bouton défini par le client à la boîte de dialogue. Lorsque le bouton est activé, MAPI appelle la fonction de rappel désignée par _lpfButtonCallback_, en passant l’identificateur de l’entrée du bouton et les données _lpvButtonContext_. Si vous n’avez pas besoin d’un bouton extensible, _lpszButtonText_ doit être NULL. 
  
 **Détails** prend en charge les chaînes de caractères Unicode ; Les chaînes Unicode sont convertis au format de chaîne (MBCS) codés avant qu’elles sont affichées dans la boîte de dialogue Détails. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnOpenEntryID  <br/> |MFCMAPI utilise la méthode **Details** pour afficher une boîte de dialogue qui affiche les détails d’une entrée de carnet d’adresses.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[ADRPARM](adrparm.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

