---
title: HrGetGALFromEmsmdbUID
description: Retourne l’identificateur d’entrée du carnet d’adresses global pour le service Exchange identifié par pEmsmdbUID.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 9b824e70-ed9a-490c-b777-8902a793fece
ms.openlocfilehash: ce9c341a5a8fe94c568d1acf0e8a7a22443fc733
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817283"
---
# <a name="hrgetgalfromemsmdbuid"></a>HrGetGALFromEmsmdbUID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Retourne l’identificateur d’entrée du carnet d’adresses global pour le service Exchange identifié par _pEmsmdbUID_. L’identificateur d’entrée retourné doit être libéré à l’aide de [MAPIFreeBuffer](mapifreebuffer.md).
  
|Propriété |Valeur |
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

## <a name="parameters"></a>Paramètres

 _pSess_
  
> [in] Session IMAPISession. Il ne peut pas être NULL.
    
 _pAddrBook_
  
> [in] Carnet d’adresses utilisé pour ouvrir l’identificateur d’entrée. Il ne peut pas être NULL.
    
 _pEmsmdbUID_
  
> [in] Pointeur vers un **emsmdbUID** qui identifie la gal du service Exchange à récupérer. Si _pEmsmdbUID_ a la valeur NULL ou l’UID zéro, cette fonction obtient la gal héritée du service Exchange. 
    
 _lpcbeid_
  
> [out] Pointeur vers le nombre d’octets de l’identificateur d’entrée de la liste d’adresses globale.
    
 _lppeid_
  
> [out] Pointeur vers l’identificateur d’entrée de la liste d’adresses globale. Cela doit être libéré à l’aide de [MAPIFreeBuffer](mapifreebuffer.md).
    

