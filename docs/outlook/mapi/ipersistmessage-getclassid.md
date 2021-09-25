---
title: IPersistMessageGetClassID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPersistMessage.GetClassID
api_type:
- COM
ms.assetid: 77eeb468-3432-4ccd-9c1e-1df9ce605193
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5d8f4283d2cf9e5de7547264de429ef8b17d9667
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561438"
---
# <a name="ipersistmessagegetclassid"></a>IPersistMessage::GetClassID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie un identificateur qui représente le serveur de formulaires qui peut gérer le formulaire. 
  
```cpp
HRESULT GetClassID(
  LPCLSID lpClassID
);
```

## <a name="parameters"></a>Paramètres

 _lpClassID_
  
> [in, out] Pointeur vers l’identificateur de classe (CLSID) du formulaire.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’identificateur de classe a été renvoyé avec succès.
    
## <a name="remarks"></a>Remarques

La **méthode IPersistMessge::GetClassID** définit le contenu du paramètre  _lpClassID_ sur l’identificateur de classe du serveur de formulaire et renvoie S_OK. Lorsqu’une visionneuse de formulaire appelle **GetClassID** et qu’elle renvoie correctement, le formulaire est placé dans [l’état Nonnitialisé.](uninitialized-state.md) 
  
Pour plus d’informations sur l’utilisation des identificateurs de classe avec des objets de stockage structuré, voir la documentation de la méthode [IPersist::GetClassID.](https://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) 
  
## <a name="see-also"></a>Voir aussi



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

