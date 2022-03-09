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
ms.openlocfilehash: 619488ecdcdbf554e8c379b45ec5544c8d8c4238
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63372548"
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

La **méthode IPersistMessge::GetClassID** définit le contenu du paramètre  _lpClassID_ sur l’identificateur de classe du serveur de formulaire et renvoie S_OK. Lorsqu’une visionneuse de formulaire appelle **GetClassID** et qu’elle renvoie correctement, le formulaire est placé dans [l’état Nonnitialisé](uninitialized-state.md) . 
  
Pour plus d’informations sur l’utilisation des identificateurs de classe avec des objets de stockage structuré, voir la documentation de la méthode [IPersist::GetClassID](https://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) . 
  
## <a name="see-also"></a>Voir aussi



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

