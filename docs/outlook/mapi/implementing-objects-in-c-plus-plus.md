---
title: Implémentation des objets dans C++
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d1a050ff-3cf9-4bf7-812d-b7c1b31056e7
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 89247ca1b263d6f06af73f1ffa14709a2aff23de
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310149"
---
# <a name="implementing-objects-in-c"></a><span data-ttu-id="fc56c-103">Implémentation des objets dans C++</span><span class="sxs-lookup"><span data-stu-id="fc56c-103">Implementing objects in C++</span></span>

<span data-ttu-id="fc56c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc56c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc56c-105">Les fournisseurs de services et les clients C++ définissent les objets MAPI en créant des classes qui héritent des interfaces qu'ils implémentent.</span><span class="sxs-lookup"><span data-stu-id="fc56c-105">C++ clients and service providers define MAPI objects by creating classes that inherit from the interfaces they are implementing.</span></span> <span data-ttu-id="fc56c-106">Chacune des méthodes d'interface est public, de même que le constructeur et le destructeur de la classe.</span><span class="sxs-lookup"><span data-stu-id="fc56c-106">Each of the interface methods is public, as are the constructor and destructor for the class.</span></span> <span data-ttu-id="fc56c-107">Si la classe possède des méthodes supplémentaires, elles peuvent être publiques ou privées, en fonction de l'implémentation.</span><span class="sxs-lookup"><span data-stu-id="fc56c-107">If the class has additional methods, they can be public or private, depending on the implementation.</span></span> <span data-ttu-id="fc56c-108">Tous les membres de données sont privés.</span><span class="sxs-lookup"><span data-stu-id="fc56c-108">All data members are private.</span></span> 
  
<span data-ttu-id="fc56c-109">L'exemple de code suivant montre comment définir un objet d'État C++.</span><span class="sxs-lookup"><span data-stu-id="fc56c-109">The following example code shows how to define a C++ status object.</span></span> <span data-ttu-id="fc56c-110">La `CMyMAPIObject` classe hérite de l'interface [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="fc56c-110">The  `CMyMAPIObject` class inherits from the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="fc56c-111">De nombreuses macros utilisées dans cet exemple sont définies dans le fichier d'en-tête OLE compobj. h.</span><span class="sxs-lookup"><span data-stu-id="fc56c-111">Many of the macros used in this example are defined in the OLE header file Compobj.h.</span></span> <span data-ttu-id="fc56c-112">Les premiers membres de la classe sont les méthodes de l'interface de base, suivies des méthodes des interfaces héritées par ordre d'héritage.</span><span class="sxs-lookup"><span data-stu-id="fc56c-112">The first members of the class are the methods of the base interface, followed by the methods of the inherited interfaces in order of inheritance.</span></span> <span data-ttu-id="fc56c-113">Le suivi des définitions d'interface est une méthode supplémentaire, le constructeur et le destructeur, ainsi que les membres de données.</span><span class="sxs-lookup"><span data-stu-id="fc56c-113">Following the interface definitions are any additional methods, the constructor and destructor, and the data members.</span></span> 
  
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

<span data-ttu-id="fc56c-114">Pour utiliser une instance de la `CMyMAPIObject` classe, les clients C++ ou les fournisseurs de services effectuent un appel à l'une de ses méthodes comme suit:</span><span class="sxs-lookup"><span data-stu-id="fc56c-114">To use an instance of the  `CMyMAPIObject` class, C++ clients or service providers make a call to one of its methods as follows:</span></span> 
  
```cpp
lpMyObj->ValidateState(ulUIParam, ulFlags);

```

## <a name="see-also"></a><span data-ttu-id="fc56c-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc56c-115">See also</span></span>

- [<span data-ttu-id="fc56c-116">Implémentation d'objets MAPI</span><span class="sxs-lookup"><span data-stu-id="fc56c-116">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

