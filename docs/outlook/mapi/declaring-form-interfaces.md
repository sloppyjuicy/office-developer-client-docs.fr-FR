---
title: Déclaration d’interfaces de formulaire
manager: lindalu
ms.date: 03/16/2022
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 79283301-e544-4a4d-96c2-3f81dc5b3731
ms.openlocfilehash: c9609e21d323e1289690e8cb77cfdae64f1bdb0f
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63521553"
---
# <a name="declaring-form-interfaces"></a>Déclaration d’interfaces de formulaire

**S’applique à** : Outlook 2013 | Outlook 2016
  
Vous pouvez simplifier les déclarations de vos implémentations d’interfaces de formulaire MAPI à l’aide des macros MAPI_interface_METHOD, où _l’interface_ est une interface de formulaire définie dans le fichier d’en-tête Mapiform.h. Vous n’êtes pas obligé d’utiliser ces macros, mais si ce n’est pas le cas, vous devez particulièrement vous occuper que vos déclarations soient conformes aux déclarations dans le fichier d’en-tête Mapiform.h. Par exemple, vous pouvez déclarer la classe d’objet de formulaire de votre serveur de formulaires comme suit :
  
```cppclass CMyForm : public IPersistMessage, public IMAPIForm,
                public IMAPIFormAdviseSink
{
public:
    CMyForm(CClassFactory *);    // constructor takes a class factory object
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
