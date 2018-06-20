---
title: IPersistMessageGetClassID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.GetClassID
api_type:
- COM
ms.assetid: 77eeb468-3432-4ccd-9c1e-1df9ce605193
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: e0937eed2e8ca61bc18ee45ff20337267808ea70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784355"
---
# <a name="ipersistmessagegetclassid"></a>IPersistMessage::GetClassID

  
  
**S’applique à**: Outlook 
  
Renvoie un identificateur qui représente le serveur de formulaire qui peut gérer le formulaire. 
  
```cpp
HRESULT GetClassID(
  LPCLSID lpClassID
);
```

## <a name="parameters"></a>Paramètres

 _lpClassID_
  
> [entrée, sortie] Pointeur vers l’identificateur de classe (CLSID) du formulaire.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’identificateur de classe a été renvoyée avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IPersistMessge::GetClassID** définit le contenu du paramètre _lpClassID_ sur l’identificateur de classe du serveur du formulaire et renvoie S_OK. Lorsqu’une visionneuse de formulaire appelle **GetClassID** et elle renvoie avec succès, le formulaire est placé dans l’état [Uninitialized](uninitialized-state.md) . 
  
Pour plus d’informations sur l’utilisation des identificateurs de classe des objets de stockage structuré, consultez la documentation de la méthode [IPersist::GetClassID](http://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) . 
  
## <a name="see-also"></a>Voir aussi



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

