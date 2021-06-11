---
title: HrGetGALFromEmsmdbUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9b824e70-ed9a-490c-b777-8902a793fece
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b9a31fec93ec7fafc4d1565d63e4bc427ba4050e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439106"
---
# <a name="hrgetgalfromemsmdbuid"></a>HrGetGALFromEmsmdbUID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie l’identificateur d’entrée du carnet d’adresses global pour le service Exchange identifié par _pEmsmdbUID_. L’identificateur d’entrée renvoyé doit être libéré à l’aide [de MAPIFreeBuffer](mapifreebuffer.md).
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |abhelp.h  <br/> |
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

## <a name="parameters"></a>Parameters

 _pSess_
  
> [in] IMAPISession connecté. Elle ne peut pas être NULL.
    
 _pAddrBook_
  
> [in] Carnet d’adresses utilisé pour ouvrir l’identificateur d’entrée. Elle ne peut pas être NULL.
    
 _pEmsmdbUID_
  
> [in] Pointeur vers **un emsmdbUID** qui identifie la LA GAL du service Exchange à récupérer. Si _pEmsmdbUID_ a la valeur NULL ou l’UID zéro, cette fonction obtient la LAL héritée du service Exchange service. 
    
 _lpcbeid_
  
> [out] Pointeur vers le nombre d’byte de l’identificateur d’entrée de la liste d’adresses globale.
    
 _lppeid_
  
> [out] Pointeur vers l’identificateur d’entrée de la liste d’adresses globale. Cela doit être libéré à [l’aide de MAPIFreeBuffer](mapifreebuffer.md).
    

