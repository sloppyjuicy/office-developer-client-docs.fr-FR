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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c90b569414c1710cc1065fdb4fd72738e265ebff
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588831"
---
# <a name="removepreprocessinfo"></a>RemovePreprocessInfo

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Supprime prétraités écrites par une fonction [PreprocessMessage](preprocessmessage.md) en fonction d’un message d’informations. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi.h  <br/> |
|Fonction implémentée par :  <br/> |Fournisseurs de transport  <br/> |
|Fonction appelée par :  <br/> |Spouleur MAPI  <br/> |
   
```cpp
HRESULT RemovePreprocessInfo(
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a>Paramètres

 _lpMessage_
  
> [in] Pointeur vers le message prétraité à partir duquel les informations sont à supprimer.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Informations prétraitées a été supprimées.
    
## <a name="remarks"></a>Remarques

Le spouleur MAPI appelle une fonction basée sur **RemovePreprocessInfo**. Un fournisseur de transport enregistre la fonction **RemovePreprocessInfo** basé en même temps qu’il enregistre la fonction **PreprocessMessage** en parallèle dans un appel à la méthode [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) . 
  
Une image de rendu qui convient pour la transmission de télécopie est un exemple d’information prétraité écrit par une fonction définie par le prototype de fonction [PreprocessMessage](preprocessmessage.md). Généralement, le spouleur MAPI appelle une fonction **RemovePreprocessInfo** après l’envoi d’un message qui contient des informations prétraitées. 
  

