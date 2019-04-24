---
title: Déclaration des interfaces de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79283301-e544-4a4d-96c2-3f81dc5b3731
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 0fa742b7ff6d98e3a0f475accbc440d22eac0919
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337057"
---
# <a name="declaring-form-interfaces"></a><span data-ttu-id="30d25-103">Déclaration des interfaces de formulaire</span><span class="sxs-lookup"><span data-stu-id="30d25-103">Declaring Form Interfaces</span></span>

  
  
<span data-ttu-id="30d25-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30d25-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30d25-105">Vous pouvez simplifier les déclarations de vos implémentations d'interfaces de formulaire MAPI à l'aide des macros _interface__METHOD MAPI_, où _interface_ est une interface de formulaire définie dans le fichier d'en-tête MAPIForm. h.</span><span class="sxs-lookup"><span data-stu-id="30d25-105">You can simplify the declarations of your implementations of MAPI form interfaces by using the MAPI_ _interface__METHOD macros, where  _interface_ is a form interface defined in the Mapiform.h header file.</span></span> <span data-ttu-id="30d25-106">Vous n'êtes pas obligé d'utiliser ces macros, mais si vous ne le faites pas, nous vous recommandons de veiller à ce que vos déclarations soient conformes aux déclarations dans le fichier d'en-tête MAPIForm. h.</span><span class="sxs-lookup"><span data-stu-id="30d25-106">You are not required to use these macros, but if you do not, you should take particular care that your declarations conform to the declarations in the Mapiform.h header file.</span></span> <span data-ttu-id="30d25-107">Par exemple, vous pouvez déclarer la classe d'objet Form de votre serveur de formulaire comme suit:</span><span class="sxs-lookup"><span data-stu-id="30d25-107">For example, you could declare your form server's form object class like the following:</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="30d25-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30d25-108">See also</span></span>



[<span data-ttu-id="30d25-109">Écriture de code de serveur de formulaire</span><span class="sxs-lookup"><span data-stu-id="30d25-109">Writing Form Server Code</span></span>](writing-form-server-code.md)

