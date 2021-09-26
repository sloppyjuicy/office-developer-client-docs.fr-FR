---
title: RemovePreprocessInfo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.RemovePreprocessInfo
api_type:
- COM
ms.assetid: 25f46937-abac-4a0b-83db-eeac9451c112
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 827f13571babdebf4fca8255575e811fda9992db
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599136"
---
# <a name="removepreprocessinfo"></a>RemovePreprocessInfo

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Supprime d’un message les informations prétraitées écrites par une fonction [preprocessMessage.](preprocessmessage.md) 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi.h  <br/> |
|Fonction définie implémentée par :  <br/> |Fournisseurs de transport  <br/> |
|Fonction définie appelée par :  <br/> |Pooler MAPI  <br/> |
   
```cpp
HRESULT RemovePreprocessInfo(
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a>Paramètres

 _lpMessage_
  
> [in] Pointeur vers le message prétraité à partir duquel les informations doivent être supprimées.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Les informations prétraitées ont été supprimées avec succès.
    
## <a name="remarks"></a>Remarques

Lepooler MAPI appelle une fonction basée sur **RemovePreprocessInfo**. Un fournisseur de transport inscrit la fonction basée **removePreprocessInfo** en même temps qu’il inscrit la fonction **basée sur PreprocessMessage** parallèle dans un appel à la méthode [IMAPISupport::RegisterPreprocessor.](imapisupport-registerpreprocessor.md) 
  
Un rendu d’image approprié pour la transmission de télécopie est un exemple d’informations prétraitées écrites par une fonction définie par le prototype de fonction [PreprocessMessage.](preprocessmessage.md) Lepooler MAPI appelle généralement une **fonction RemovePreprocessInfo** après l’envoi d’un message contenant des informations prétraitées. 
  

