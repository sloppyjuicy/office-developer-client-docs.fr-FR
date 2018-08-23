---
title: HrGetGALFromEmsmdbUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9b824e70-ed9a-490c-b777-8902a793fece
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 4b05baf1f819a821da3496cc63c2b2980894efd7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575713"
---
# <a name="hrgetgalfromemsmdbuid"></a>HrGetGALFromEmsmdbUID

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Renvoie l’identificateur d’entrée du carnet d’adresses globale pour le service Exchange identifié par _pEmsmdbUID_. L’identificateur d’entrée renvoyée doit être libéré à l’aide de [MAPIFreeBuffer](mapifreebuffer.md).
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |abhelp.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
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
  
> [in] La session IMAPISession. Il ne peut pas être NULL.
    
 _pAddrBook_
  
> [in] Le carnet d’adresses utilisée pour ouvrir l’identificateur d’entrée. Il ne peut pas être NULL.
    
 _pEmsmdbUID_
  
> [in] Pointeur vers un **emsmdbUID** qui identifie la liste d’adresses globale du Service Exchange à récupérer. Si _pEmsmdbUID_ est NULL ou l’UID de zéro, cette fonction obtient la liste d’adresses globale héritée du Service Exchange. 
    
 _lpcbeid_
  
> [out] Pointeur vers le nombre d’octets de l’identificateur d’entrée de la liste d’adresses globale.
    
 _lppeid_
  
> [out] Pointeur vers l’identificateur d’entrée de la liste d’adresses globale. Il doit être libéré à l’aide de [MAPIFreeBuffer](mapifreebuffer.md).
    

