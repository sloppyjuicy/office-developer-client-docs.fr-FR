---
title: Déclaration d’Interfaces de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79283301-e544-4a4d-96c2-3f81dc5b3731
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 8f4d8842efbba2f1f2b7281e5d4741b89f975b3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783126"
---
# <a name="declaring-form-interfaces"></a>Déclaration d’Interfaces de formulaire

  
  
**S’applique à**: Outlook 
  
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



[Écriture de Code de formulaire Server](writing-form-server-code.md)

