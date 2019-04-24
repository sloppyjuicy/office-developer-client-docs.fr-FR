---
title: RemovePreprocessInfo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.RemovePreprocessInfo
api_type:
- COM
ms.assetid: 25f46937-abac-4a0b-83db-eeac9451c112
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d80c73aef780a0da39f3939f71462488a067de5f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328377"
---
# <a name="removepreprocessinfo"></a>RemovePreprocessInfo

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Supprime les informations prétraitées écrites par une fonction basée sur [PreprocessMessage](preprocessmessage.md) à partir d'un message. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi. h  <br/> |
|Fonction définie implémentée par:  <br/> |Fournisseurs de transport  <br/> |
|Fonction définie appelée par:  <br/> |Spouleur MAPI  <br/> |
   
```cpp
HRESULT RemovePreprocessInfo(
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a>Paramètres

 _lpMessage_
  
> dans Pointeur vers le message prétraité à partir duquel les informations doivent être supprimées.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Les informations prétraitées ont été supprimées.
    
## <a name="remarks"></a>Remarques

Le spouleur MAPI appelle une fonction basée sur **RemovePreprocessInfo**. Un fournisseur de transport enregistre la fonction basée sur **RemovePreprocessInfo** en même temps qu'il enregistre la fonction **PreprocessMessage** en parallèle dans un appel à la méthode [IMAPISupport:: RegisterPreprocessor](imapisupport-registerpreprocessor.md) . 
  
Un rendu d'image adapté à la transmission de télécopie est un exemple d'informations prétraitées écrites par une fonction définie par le prototype de fonction [PreprocessMessage](preprocessmessage.md). Le spouleur MAPI appelle généralement une fonction **RemovePreprocessInfo** après l'envoi d'un message qui contient des informations prétraitées. 
  

