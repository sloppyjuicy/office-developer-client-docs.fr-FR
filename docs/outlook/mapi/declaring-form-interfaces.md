---
title: Déclaration d’interfaces de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79283301-e544-4a4d-96c2-3f81dc5b3731
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 0fa742b7ff6d98e3a0f475accbc440d22eac0919
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437510"
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

