---
title: IAddrBookDetails
description: La fonction IAddrBookDetails affiche une boîte de dialogue qui affiche des détails sur une entrée de carnet d’adresses particulière.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook.Details
api_type:
- COM
ms.assetid: 4eee4382-98c3-4714-8920-8d72edef00b8
ms.openlocfilehash: 17005b0ad74a23f185ce9ba868708bd81b6ecf07
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816401"
---
# <a name="iaddrbookdetails"></a>IAddrBook::Details

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

## <a name="parameters"></a>Paramètres

 _lpulUIParam_

> [in] Pointeur vers un handle de la fenêtre parente de la boîte de dialogue.

 _lpfnDismiss_
 
> [in] Pointeur vers une fonction basée sur le prototype [DISMISSMODELESS](dismissmodeless.md) , ou NULL. Ce membre s’applique uniquement à la version sans mode de la boîte de dialogue, comme indiqué par l’indicateur DIALOG_SDI en cours de définition. MAPI appelle la fonction **DISMISSMODELESS** lorsque l’utilisateur ignore la boîte de dialogue d’adresse sans mode, informant un client qui appelle **Details** que la boîte de dialogue n’est plus active.

 _lpvDismissContext_
 
> [in] Pointeur vers les informations de contexte à passer à la fonction **DISMISSMODELESS** pointée par le paramètre  _lpfnDismiss_ . Ce paramètre s’applique uniquement à la version sans mode de la boîte de dialogue, en incluant l’indicateur DIALOG_SDI dans le paramètre _ulFlags_ .

 _cbEntryID_
 
> [in] Nombre d’octets dans l’identificateur d’entrée pointé par le paramètre  _lpEntryID_ .

 _lpEntryID_
 
> [in] Pointeur vers l’identificateur d’entrée de l’entrée pour laquelle les détails sont affichés.

 _lpfButtonCallback_
 
> [in] Pointeur vers une fonction basée sur le prototype de fonction [LPFNBUTTON](lpfnbutton.md) . Une fonction **LPFNBUTTON** ajoute un bouton à la boîte de dialogue détails.

 _lpvButtonContext_

> [in] Pointeur vers les données utilisées comme paramètre pour la fonction spécifiée par le paramètre _lpfButtonCallback_ .

 _lpszButtonText_

> [in] Pointeur vers une chaîne qui contient du texte à appliquer au bouton ajouté, si ce bouton est extensible. Le paramètre _lpszButtonText_ doit être NULL si vous n’avez pas besoin d’un bouton extensible.

 _ulFlags_

> [in] Masque de bits des indicateurs qui contrôle le type du texte pour le paramètre _lpszButtonText_ . Les indicateurs suivants peuvent être définis :

AB_TELL_DETAILS_CHANGE

> Indique que **Details** retourne S_OK si des modifications sont réellement apportées à l’adresse ; sinon, **Details** retourne S_FALSE.

DIALOG_MODAL

> Affichez la version modale de la boîte de dialogue d’adresse commune, qui est toujours affichée dans les clients non Outlook. Cet indicateur s’exclue mutuellement de DIALOG_SDI.

DIALOG_SDI

> Affichez la version sans mode de la boîte de dialogue d’adresse commune. Cet indicateur est ignoré pour les clients non Outlook.

MAPI_UNICODE

> Les chaînes passées sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas défini, les chaînes sont au format ANSI.

## <a name="return-value"></a>Valeur renvoyée

S_OK

> La boîte de dialogue Détails a été affichée avec succès pour l’entrée du carnet d’adresses.

## <a name="remarks"></a>Remarques

Les applications clientes appellent la méthode **Details** pour afficher une boîte de dialogue qui fournit des détails sur une entrée particulière dans le carnet d’adresses. Vous pouvez utiliser les paramètres _lpfButtonCallback_, _lpvButtonContext_ et _lpszButtonText_ pour ajouter un bouton défini par le client à la boîte de dialogue. Lorsque vous cliquez sur le bouton, MAPI appelle la fonction de rappel pointée par _lpfButtonCallback_, en passant à la fois l’identificateur d’entrée du bouton et les données dans _lpvButtonContext_. Si vous n’avez pas besoin d’un bouton extensible, _lpszButtonText_ doit avoir la valeur NULL.
  
 **Details** prend en charge les chaînes de caractères Unicode ; Les chaînes Unicode sont converties au format de chaîne de caractères multioctets (MBCS) avant d’être affichées dans la boîte de dialogue de détails.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnOpenEntryID  <br/> |MFCMAPI utilise la méthode **Details** pour afficher une boîte de dialogue qui affiche les détails d’une entrée de carnet d’adresses. |

## <a name="see-also"></a>Voir aussi

[ADRPARM](adrparm.md)

[IAddrBook::Address](iaddrbook-address.md)

[LPFNBUTTON](lpfnbutton.md)

[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
