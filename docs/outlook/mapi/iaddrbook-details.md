---
title: IAddrBookDetails
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d52027195ee898cadd63ca686d944eb792873755
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63380822"
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
 
> [in] Pointeur vers une fonction basée sur le prototype [DISMISSMODELESS](dismissmodeless.md) ou NULL. Ce membre s’applique uniquement à la version sans mode de la boîte de dialogue, comme indiqué par l’indicateur DIALOG_SDI en cours de mise en place. MAPI appelle la **fonction DISMISSMODELESS** lorsque l’utilisateur fait disparaître la boîte de dialogue d’adresses sans mode, informant un client qui appelle **Details** que la boîte de dialogue n’est plus active.

 _lpvDismissContext_
 
> [in] Pointeur vers les informations de contexte à transmettre à la **fonction DISMISSMODELESS** pointée par  _le paramètre lpfnDismiss_ . Ce paramètre s’applique uniquement à la version sans mode de la boîte de dialogue, en incluant l’indicateur DIALOG_SDI dans le _paramètre ulFlags_ .

 _cbEntryID_
 
> [in] Nombre d’bytes dans l’identificateur d’entrée pointé par  _le paramètre lpEntryID_ .

 _lpEntryID_
 
> [in] Pointeur vers l’identificateur d’entrée pour lequel les détails sont affichés.

 _lpfButtonCallback_
 
> [in] Pointeur vers une fonction basée sur le prototype [de fonction LPFNBUTTON](lpfnbutton.md) . Une **fonction LPFNBUTTON** ajoute un bouton à la boîte de dialogue Détails.

 _lpvButtonContext_

> [in] Pointeur vers des données qui a été utilisé comme paramètre pour la fonction spécifiée par _le paramètre lpfButtonCallback_ .

 _lpszButtonText_

> [in] Pointeur vers une chaîne qui contient du texte à appliquer au bouton ajouté, si ce bouton est extensible. Le _paramètre lpszButtonText_ doit être NULL si vous n’avez pas besoin d’un bouton extensible.

 _ulFlags_

> [in] Masque de bits d’indicateurs qui contrôle le type du texte pour le _paramètre lpszButtonText_ . Les indicateurs suivants peuvent être définies :

AB_TELL_DETAILS_CHANGE

> Indique que **les détails renvoient** S_OK si des modifications sont réellement apportées à l’adresse ; Dans le **cas contraire, les détails** renvoient S_FALSE.

DIALOG_MODAL

> Affichez la version modale de la boîte de dialogue d’adresses commune, qui est toujours affichée dans les clients Outlook non privés. Cet indicateur s’exclue mutuellement avec DIALOG_SDI.

DIALOG_SDI

> Affiche la version non modée de la boîte de dialogue d’adresse commune. Cet indicateur est ignoré pour les clients non Outlook client.

MAPI_UNICODE

> Les chaînes transmises sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.

## <a name="return-value"></a>Valeur renvoyée

S_OK

> La boîte de dialogue Détails a été affichée avec succès pour l’entrée du carnet d’adresses.

## <a name="remarks"></a>Remarques

Les applications clientes **appellent la méthode Details** pour afficher une boîte de dialogue qui fournit des détails sur une entrée particulière dans le carnet d’adresses. Vous pouvez utiliser les paramètres _lpfButtonCallback_, _lpvButtonContext_ et _lpszButtonText_ pour ajouter un bouton défini par le client à la boîte de dialogue. Lorsque vous cliquez sur le bouton, MAPI appelle la fonction de rappel pointée par _lpfButtonCallback_, en passant l’identificateur d’entrée du bouton et les données dans _lpvButtonContext_. Si vous n’avez pas besoin d’un bouton extensible, _lpszButtonText_ doit être NULL.
  
 **Les détails prend** en charge les chaînes de caractères Unicode ; Les chaînes Unicode sont converties au format de chaîne de caractères multioctets (MBCS) avant d’être affichées dans la boîte de dialogue d’informations.
  
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
