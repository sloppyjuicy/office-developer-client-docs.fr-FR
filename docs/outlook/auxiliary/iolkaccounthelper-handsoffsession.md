---
title: IOlkAccountHelperHandsOffSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 9f71fdef-5df5-0892-b64c-293a2f22f5c3
description: Libère l’objet de session MAPI renvoyé par IOlkAccountHelper::GetMapiSession.
ms.openlocfilehash: 3909d65d516d2b2da8e215bf5504e0ab64faa374
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617117"
---
# <a name="iolkaccounthelperhandsoffsession"></a>IOlkAccountHelper::HandsOffSession

Libère l’objet de session MAPI qui a été renvoyé par - [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccountHelper](iolkaccounthelper.md).
  
```cpp
HRESULT IOlkAccountHelper::HandsOffSession( );
```

## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Si votre implémentation **d’IOlkAccountHelper** crée sa propre session MAPI qui est renvoyée dans **IOlkAccountHelper::GetMapiSession,** vous devez libérer la session ici et renvoyer S_OK.  <br/> |
|E_NOTIMPL  <br/> |Si votre implémentation **d’IOlkAccountHelper** n’a pas créé sa propre session MAPI, vous devez renvoyer uniquement E_NOTIMPL. Dans ce cas, il s’agit de la seule valeur de retour prise en charge.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md)  
- [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md)

