---
title: Déclaration d’interfaces de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 79283301-e544-4a4d-96c2-3f81dc5b3731
ms.openlocfilehash: ad19db71a09f6f73289c1c1ed973f8bda52d3e09
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63372345"
---
# <a name="declaring-form-interfaces"></a>Déclaration d’interfaces de formulaire

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Vous pouvez simplifier les déclarations de vos implémentations d’interfaces de formulaire MAPI à l’aide des macros MAPI_ _interface__METHOD, où  _l’interface_ est une interface de formulaire définie dans le fichier d’en-tête Mapiform.h. Vous n’êtes pas obligé d’utiliser ces macros, mais si ce n’est pas le cas, vous devez particulièrement vous occuper que vos déclarations soient conformes aux déclarations dans le fichier d’en-tête Mapiform.h. Par exemple, vous pouvez déclarer la classe d’objet de formulaire de votre serveur de formulaires comme suit : 
  
```cpp
class CMyForm : public IPersistMessage, public IMAPIForm,
                public IMAPIFormAdviseSink
{
public:
    CMyForm(CClassFactory *);    // constructorr takes a class factory object
    ~CMyForm(void);
// MAPI methods that need to be implemented.
    MAPI_IUNKNOWN_METHODS(IMPL);
    MAPI_GETLASTERROR_METHOD(IMPL);
    MAPI_IPERSISTMESSAGE_METHODS(IMPL);
    MAPI_IMAPIFORM_METHODS(IMPL);
    MAPI_IMAPIFORMADVISESINK_METHODS(IMPL);
// Add other implementation specific items.
};

```

## <a name="see-also"></a>Voir aussi



[Écriture de code serveur de formulaire](writing-form-server-code.md)

