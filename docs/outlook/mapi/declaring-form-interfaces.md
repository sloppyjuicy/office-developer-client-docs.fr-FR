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
ms.openlocfilehash: 4687b07c89d866acbe3b6a8f4cde3262657a06b5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584246"
---
# <a name="declaring-form-interfaces"></a>Déclaration d’interfaces de formulaire

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Vous pouvez simplifier les déclarations de vos mises en œuvre des interfaces de formulaire MAPI en utilisant les macros _interface__METHOD MAPI_, où _interface_ est un formulaire définies dans le fichier d’en-tête Mapiform.h. Vous ne devez pas utiliser ces macros, mais si vous le faites pas, vous devez prendre soin particulier vos déclarations conformes aux déclarations dans le fichier d’en-tête Mapiform.h. Par exemple, vous pouvez déclarer la classe d’objet du serveur de votre formulaire formulaire comme suit : 
  
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



[Écriture de code du serveur de formulaire](writing-form-server-code.md)

