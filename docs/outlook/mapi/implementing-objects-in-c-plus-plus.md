---
title: Implémentation des objets dans C++
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d1a050ff-3cf9-4bf7-812d-b7c1b31056e7
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 89247ca1b263d6f06af73f1ffa14709a2aff23de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432953"
---
# <a name="implementing-objects-in-c"></a><span data-ttu-id="ebfdb-103">Implémentation des objets dans C++</span><span class="sxs-lookup"><span data-stu-id="ebfdb-103">Implementing objects in C++</span></span>

<span data-ttu-id="ebfdb-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ebfdb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ebfdb-105">Les clients et fournisseurs de services C++ définissent des objets MAPI en créant des classes qui héritent des interfaces qu’ils implémentent.</span><span class="sxs-lookup"><span data-stu-id="ebfdb-105">C++ clients and service providers define MAPI objects by creating classes that inherit from the interfaces they are implementing.</span></span> <span data-ttu-id="ebfdb-106">Chacune des méthodes d’interface est publique, tout comme le constructeur et le destructeur de la classe.</span><span class="sxs-lookup"><span data-stu-id="ebfdb-106">Each of the interface methods is public, as are the constructor and destructor for the class.</span></span> <span data-ttu-id="ebfdb-107">Si la classe dispose de méthodes supplémentaires, elles peuvent être publiques ou privées, selon l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="ebfdb-107">If the class has additional methods, they can be public or private, depending on the implementation.</span></span> <span data-ttu-id="ebfdb-108">Tous les membres de données sont privés.</span><span class="sxs-lookup"><span data-stu-id="ebfdb-108">All data members are private.</span></span> 
  
<span data-ttu-id="ebfdb-109">L’exemple de code suivant montre comment définir un objet d’état C++.</span><span class="sxs-lookup"><span data-stu-id="ebfdb-109">The following example code shows how to define a C++ status object.</span></span> <span data-ttu-id="ebfdb-110">La `CMyMAPIObject` classe hérite de l’interface [IMAPIStatus : IMAPIProp.](imapistatusimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="ebfdb-110">The  `CMyMAPIObject` class inherits from the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="ebfdb-111">De nombreuses macros utilisées dans cet exemple sont définies dans le fichier d’en-tête OLE Compo ren.h.</span><span class="sxs-lookup"><span data-stu-id="ebfdb-111">Many of the macros used in this example are defined in the OLE header file Compobj.h.</span></span> <span data-ttu-id="ebfdb-112">Les premiers membres de la classe sont les méthodes de l’interface de base, suivies des méthodes des interfaces héritées par ordre d’héritage.</span><span class="sxs-lookup"><span data-stu-id="ebfdb-112">The first members of the class are the methods of the base interface, followed by the methods of the inherited interfaces in order of inheritance.</span></span> <span data-ttu-id="ebfdb-113">Les définitions d’interface suivantes sont les méthodes supplémentaires, le constructeur et le destructeur, ainsi que les membres de données.</span><span class="sxs-lookup"><span data-stu-id="ebfdb-113">Following the interface definitions are any additional methods, the constructor and destructor, and the data members.</span></span> 
  
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

<span data-ttu-id="ebfdb-114">Pour utiliser une instance de la classe, les clients ou fournisseurs de services C++ appellent l’une de ses méthodes  `CMyMAPIObject` comme suit :</span><span class="sxs-lookup"><span data-stu-id="ebfdb-114">To use an instance of the  `CMyMAPIObject` class, C++ clients or service providers make a call to one of its methods as follows:</span></span> 
  
```cpp
lpMyObj->ValidateState(ulUIParam, ulFlags);

```

## <a name="see-also"></a><span data-ttu-id="ebfdb-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebfdb-115">See also</span></span>

- [<span data-ttu-id="ebfdb-116">Mise en œuvre des objets MAPI</span><span class="sxs-lookup"><span data-stu-id="ebfdb-116">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

