---
title: HrGetGALFromEmsmdbUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9b824e70-ed9a-490c-b777-8902a793fece
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: b9a31fec93ec7fafc4d1565d63e4bc427ba4050e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347830"
---
# <a name="hrgetgalfromemsmdbuid"></a>HrGetGALFromEmsmdbUID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie l'identificateur d'entrée du carnet d'adresses global pour le service Exchange identifié par _pEmsmdbUID_. L'identificateur d'entrée retourné doit être libéré à l'aide de [MAPIFreeBuffer](mapifreebuffer.md).
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |abhelp. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
HRESULT HrGetGALFromEmsmdbUID(
  LPMAPISESSION pSess,
  LPADRBOOK lpAdrBook,
  const MAPIUID * pEmsmdbUID,
  ULONG * lpcbeid,
  LPENTRYID * lppeid
);
```

## <a name="parameters"></a>Paramètres

 _pSess_
  
> dans Le IMAPISession connecté. Il ne peut pas être NULL.
    
 _pAddrBook_
  
> dans Carnet d'adresses utilisé pour ouvrir l'identificateur d'entrée. Il ne peut pas être NULL.
    
 _pEmsmdbUID_
  
> dans Pointeur vers un **emsmdbUID** qui identifie la liste d'adresses globale du service Exchange à récupérer. Si _pEmsmdbUID_ est null ou zéro uid, cette fonction obtient la lag héritée du service Exchange. 
    
 _lpcbeid_
  
> remarquer Pointeur vers le nombre d'octets de l'identificateur d'entrée de la liste d'adresses globale.
    
 _lppeid_
  
> remarquer Pointeur vers l'identificateur d'entrée de la liste d'adresses globale. Cela doit être libéré à l'aide de [MAPIFreeBuffer](mapifreebuffer.md).
    

