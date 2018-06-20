---
title: IABProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABProvider.Shutdown
api_type:
- COM
ms.assetid: 1fbe6dc1-254b-4557-92c8-9fa42a8efd64
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 2f1872c6f95f8ab12014de9890b0d03789bc5f0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783613"
---
# <a name="iabprovidershutdown"></a>IABProvider::Shutdown

  
  
**S’applique à**: Outlook 
  
Annule une connexion à une session active.
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpulFlags_
  
> [In] Réservé ; doit être un pointeur vers zéro.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La connexion a été annulée.
    
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Dans votre implémentation de la méthode **Shutdown** , effectuez toutes les tâches estiment nécessaires. MAPI appelle votre méthode **Shutdown** uniquement une fois que vous avez publié tous les objets d’ouverture de session. 
  
## <a name="see-also"></a>Voir aussi



[IABProvider : IUnknown](iabprovideriunknown.md)

