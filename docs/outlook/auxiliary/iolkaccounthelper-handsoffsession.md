---
title: IOlkAccountHelperHandsOffSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9f71fdef-5df5-0892-b64c-293a2f22f5c3
description: "Libère l'objet session MAPI renvoyé par IOlkAccountHelper:: GetMapiSession."
ms.openlocfilehash: c481cee1ecb8c2bd3997cdee8ae86c9c3b5a712e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322091"
---
# <a name="iolkaccounthelperhandsoffsession"></a>IOlkAccountHelper::HandsOffSession

Libère l'objet session MAPI renvoyé par- [IOlkAccountHelper:: GetMapiSession](iolkaccounthelper-getmapisession.md).
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccountHelper](iolkaccounthelper.md).
  
```cpp
HRESULT IOlkAccountHelper::HandsOffSession( );
```

## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Si votre implémentation de **IOlkAccountHelper** crée sa propre session MAPI qui est renvoyée dans **IOlkAccountHelper:: GetMapiSession**, vous devez libérer la session ici et retourner S_OK.  <br/> |
|E_NOTIMPL  <br/> |Si votre implémentation de **IOlkAccountHelper** n'a pas créé sa propre session MAPI, vous devez renvoyer uniquement E_NOTIMPL. Dans ce cas, il s'agit de la seule valeur renvoyée prise en charge.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md)  
- [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md)

