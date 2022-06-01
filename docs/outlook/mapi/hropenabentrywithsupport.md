---
title: HrOpenABEntryWithSupport
description: Cet article décrit la fonction HrOpenABEntryWithSupport et fournit la syntaxe et les paramètres. N’utilisez pas cette fonction.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: eaa988ea-aee1-4066-8c78-2b6c28def5e0
ms.openlocfilehash: 094b0af5ab72b263c4c794416f8e691c5ae8fb5e
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817486"
---
# <a name="hropenabentrywithsupport"></a>HrOpenABEntryWithSupport

**S’applique à** : Outlook 2013 | Outlook 2016
  
N’utilisez pas cette fonction.
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |abhelp.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |

```cpp
HRESULT HrOpenABEntryWithSupport(
  LPMAPISUP lpSup,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID  lpInterface,
  ULONG  ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Paramètres

 _lpSup_
  
>

 _cbEntryID_
  
> [in] Nombre d’octets de l’identificateur d’entrée spécifié par le paramètre _lpEntryID_ .

 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée qui représente l’entrée de carnet d’adresses à ouvrir.

 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) de l’interface à utiliser pour accéder à l’entrée ouverte. Le passage de NULL retourne l’interface standard de l’objet. Pour les utilisateurs de messagerie, l’interface standard est [IMailUser : IMAPIProp](imailuserimapiprop.md). Pour les listes de distribution, il s’agit [d’IDistList : IMAPIContainer](idistlistimapicontainer.md), et pour les conteneurs, il s’agit [d’IABContainer : IMAPIContainer](iabcontainerimapicontainer.md). Les appelants peuvent définir _lpInterface_ sur l’interface standard appropriée ou une interface dans la hiérarchie d’héritage.

 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôle le type du texte pour le paramètre _lpszButtonText_ . Les indicateurs suivants peuvent être définis :

AB_TELL_DETAILS_CHANGE
  
> Indique que Details retourne TRUE si des modifications sont réellement apportées à l’adresse ; sinon, Details retourne FALSE.

DIALOG_MODAL
  
> Affiche la version modale de la boîte de dialogue d’adresse commune. Cet indicateur s’exclue mutuellement de DIALOG_SDI.

DIALOG_SDI
  
> Affiche la version sans mode de la boîte de dialogue d’adresse commune. Cet indicateur s’exclue mutuellement de DIALOG_MODAL.

MAPI_UNICODE
  
> Les chaînes passées sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas défini, les chaînes sont au format ANSI.

 _lpulObjType_
  
> [out] Pointeur vers le type de l’entrée ouverte.

 _lppUnk_
  
> [out] Pointeur vers un pointeur de l’entrée ouverte.
