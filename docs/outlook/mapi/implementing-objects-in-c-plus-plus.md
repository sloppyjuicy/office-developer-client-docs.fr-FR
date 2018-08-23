---
title: Implémentation d’objets en langage C++
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d1a050ff-3cf9-4bf7-812d-b7c1b31056e7
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4c233f9855674080496b2e54ba9548a53738ead8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574726"
---
# <a name="implementing-objects-in-c"></a><span data-ttu-id="0a562-103">Implémentation d’objets en langage C++</span><span class="sxs-lookup"><span data-stu-id="0a562-103">Implementing objects in C++</span></span>

<span data-ttu-id="0a562-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0a562-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0a562-105">Fournisseurs de services et les clients C++ définissent objets MAPI en créant des classes qui héritent des elles implémentent les interfaces.</span><span class="sxs-lookup"><span data-stu-id="0a562-105">C++ clients and service providers define MAPI objects by creating classes that inherit from the interfaces they are implementing.</span></span> <span data-ttu-id="0a562-106">Chacune des méthodes de l’interface est public, le constructeur et le destructeur pour la classe.</span><span class="sxs-lookup"><span data-stu-id="0a562-106">Each of the interface methods is public, as are the constructor and destructor for the class.</span></span> <span data-ttu-id="0a562-107">Si la classe dispose de méthodes supplémentaires, ils peuvent être publiques ou privées, en fonction de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="0a562-107">If the class has additional methods, they can be public or private, depending on the implementation.</span></span> <span data-ttu-id="0a562-108">Tous les membres de données sont privées.</span><span class="sxs-lookup"><span data-stu-id="0a562-108">All data members are private.</span></span> 
  
<span data-ttu-id="0a562-109">L’exemple de code suivant montre comment définir un objet d’état C++.</span><span class="sxs-lookup"><span data-stu-id="0a562-109">The following example code shows how to define a C++ status object.</span></span> <span data-ttu-id="0a562-110">Le `CMyMAPIObject` classe hérite de la [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span><span class="sxs-lookup"><span data-stu-id="0a562-110">The  `CMyMAPIObject` class inherits from the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="0a562-111">Bon nombre des macros utilisés dans cet exemple sont définies dans le fichier d’en-tête Compobj.h OLE.</span><span class="sxs-lookup"><span data-stu-id="0a562-111">Many of the macros used in this example are defined in the OLE header file Compobj.h.</span></span> <span data-ttu-id="0a562-112">Les premiers membres de la classe sont les méthodes de l’interface de base, suivi par les méthodes des interfaces dans l’ordre de l’héritage des autorisations héritées.</span><span class="sxs-lookup"><span data-stu-id="0a562-112">The first members of the class are the methods of the base interface, followed by the methods of the inherited interfaces in order of inheritance.</span></span> <span data-ttu-id="0a562-113">Les définitions d’interface sont d’autres méthodes, le constructeur et destructeur et les membres de données.</span><span class="sxs-lookup"><span data-stu-id="0a562-113">Following the interface definitions are any additional methods, the constructor and destructor, and the data members.</span></span> 
  
```cpp
class  CMyMAPIObject : public IMAPIStatus
{
public:
// Methods of IUnknown.
    STDMETHODIMP QueryInterface (REFIID riid, LPVOID * ppvObj);
    STDMETHODIMP_(ULONG) AddRef ();
    STDMETHODIMP_(ULONG) Release ();
    MAPI_IMAPIPROP_METHODS(IMPL);
    MAPI_IMAPISTATUS_METHODS(IMPL);
// Other methods specific to CMyMAPIObject.
    BOOL WINAPI Method1 ();
    void WINAPI Method2 ();
// Constructors and destructors.
public :
    CMyMAPIObject () {};
    ~CMyMAPIObject () {};
// Data members specific to CMyMAPIObject.
private :
    ULONG               m_cRef;
    CAnotherObj *       m_pObj;
};
 
```

<span data-ttu-id="0a562-114">Pour utiliser une instance de le `CMyMAPIObject` classe, clients C++ ou fournisseurs de services émettre un appel à l’une de ses méthodes, comme suit :</span><span class="sxs-lookup"><span data-stu-id="0a562-114">To use an instance of the  `CMyMAPIObject` class, C++ clients or service providers make a call to one of its methods as follows:</span></span> 
  
```cpp
lpMyObj->ValidateState(ulUIParam, ulFlags);

```

## <a name="see-also"></a><span data-ttu-id="0a562-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a562-115">See also</span></span>

- [<span data-ttu-id="0a562-116">Implémentation d’objets MAPI</span><span class="sxs-lookup"><span data-stu-id="0a562-116">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

