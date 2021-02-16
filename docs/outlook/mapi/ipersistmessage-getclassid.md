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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 3f0d98b8ffa13fe238fc0fcf8ff0ec76a3a284eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309624"
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

