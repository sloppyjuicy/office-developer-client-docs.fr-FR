---
title: IOlkAccountHelperHandsOffSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 9f71fdef-5df5-0892-b64c-293a2f22f5c3
description: Libère l’objet de session MAPI renvoyé par IOlkAccountHelper::GetMapiSession.
ms.openlocfilehash: 6b4ee9a7409e34e79800af724eebb355cfa59ec5
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62789255"
---
# <a name="iolkaccounthelperhandsoffsession"></a>IOlkAccountHelper::HandsOffSession

Libère l’objet de session MAPI renvoyé par - [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccountHelper](iolkaccounthelper.md).
  
```cpp
HRESULT IOlkAccountHelper::HandsOffSession( );
```

## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Si votre implémentation **d’IOlkAccountHelper** crée sa propre session MAPI qui est renvoyée dans **IOlkAccountHelper::GetMapiSession**, vous devez libérer la session ici et S_OK. |
|E_NOTIMPL  <br/> |Si votre implémentation **d’IOlkAccountHelper** n’a pas créé sa propre session MAPI, vous devez renvoyer uniquement E_NOTIMPL. Dans ce cas, il s’agit de la seule valeur de retour prise en charge. |
   
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md)  
- [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md)

