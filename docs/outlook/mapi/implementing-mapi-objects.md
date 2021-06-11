---
title: Mise en œuvre des objets MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b1ee2533-8077-4976-846b-d42d148bf8c6
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c0d67d10d54591de926724cbf594a44f17e9ea14
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310170"
---
# <a name="implementing-mapi-objects"></a><span data-ttu-id="6e6ff-103">Mise en œuvre des objets MAPI</span><span class="sxs-lookup"><span data-stu-id="6e6ff-103">Implementing MAPI Objects</span></span>

  
  
<span data-ttu-id="6e6ff-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e6ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e6ff-105">Les objets MAPI peuvent être implémentés à l’aide de classes C++ ou de structures de données C, en fonction du langage et de l’ensemble d’API utilisé par un client ou un fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-105">MAPI objects can be implemented by using C++ classes or C data structures, depending on the language and the API set a client or service provider is using.</span></span> <span data-ttu-id="6e6ff-106">Les fournisseurs de services peuvent être écrits en C ou C++ avec l’interface du fournisseur de services MAPI . les applications clientes peuvent également utiliser C ou C++.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-106">Service providers can be written in C or C++ with the MAPI service provider interface; client applications can also use C or C++.</span></span> <span data-ttu-id="6e6ff-107">Si possible, les clients et les fournisseurs de services qui utilisent l’interface de programmation orientée objet doivent utiliser C++.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-107">If possible, clients and service providers that use the object-oriented programming interface should use C++.</span></span> 
  
<span data-ttu-id="6e6ff-108">C++ est le choix préféré, car MAPI est une technologie orientée objet, et C++ se prête plus facilement au développement orienté objet.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-108">C++ is the preferred choice because MAPI is an object-oriented technology, and C++ lends itself more readily to object-oriented development.</span></span> <span data-ttu-id="6e6ff-109">Le code qui en résulte est plus simple et plus simple, ce qui facilite sa maintenance.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-109">The resulting code is simpler and more straightforward, making it easier to maintain.</span></span> <span data-ttu-id="6e6ff-110">La documentation MAPI est écrite principalement pour les développeurs C++. Toutes les descriptions de syntaxe pour les méthodes d’interface MAPI dans cette référence sont en C++.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-110">The MAPI documentation is written primarily for C++ developers; all of the syntax descriptions for the MAPI interface methods in this Reference are in C++.</span></span>
  
<span data-ttu-id="6e6ff-111">Les développeurs peuvent utiliser Microsoft Visual Studio et des outils de développement tiers pour développer des solutions qui appellent MAPI.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-111">Developers can use Microsoft Visual Studio and third-party development tools to develop solutions that call MAPI.</span></span> <span data-ttu-id="6e6ff-112">Notez que les développeurs doivent utiliser C ou C++ non géré, mais pas C++ géré pour écrire des solutions MAPI.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-112">Note that developers should use C or unmanaged C++, but not managed C++ to write MAPI solutions.</span></span>
  
<span data-ttu-id="6e6ff-113">Lorsqu’un objet MAPI est implémenté, un client ou un fournisseur de services crée du code pour toutes les méthodes d’interface, du code pour toutes les méthodes privées spécifiques à l’implémentation et du code pour prendre en charge les membres de données privées pour la maintenance des informations d’état.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-113">When a MAPI object is implemented, a client or service provider creates code for all of the interface methods, code for any private methods that are specific to the implementation, and code to support private data members for maintaining state information.</span></span> <span data-ttu-id="6e6ff-114">Le code des méthodes d’interface doit respecter les spécifications publiées par MAPI qui documentent le comportement attendu.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-114">The code for the interface methods must follow the specifications published by MAPI that document expected behavior.</span></span> 
  
<span data-ttu-id="6e6ff-115">Il existe de nombreuses macros dans le fichier d’en-tête Mapidefs.h et les fichiers d’en-tête OLE que les clients et fournisseurs de services dans les deux langues peuvent utiliser pour les aider avec leurs définitions d’objets MAPI.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-115">There are many macros in the Mapidefs.h header file and OLE header files that clients and service providers in either language can use to help them with their definitions of MAPI objects.</span></span> <span data-ttu-id="6e6ff-116">Par exemple, il existe une macro pour définir les méthodes de chacune des interfaces MAPI.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-116">For example, there is a macro to define the methods of each of the MAPI interfaces.</span></span> <span data-ttu-id="6e6ff-117">La macro qui définit les méthodes de l’interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) apparaît dans Mapidefs.h comme suit :</span><span class="sxs-lookup"><span data-stu-id="6e6ff-117">The macro to define the methods of the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface appears in Mapidefs.h as follows:</span></span> 
  
```cpp
#define MAPI_IUNKNOWN_METHODS(IPURE)          \
    MAPIMETHOD(QueryInterface)                \
        (THIS_ REFIID riid, LPVOID FAR * ppvObj) IPURE;    \
    MAPIMETHOD_(ULONG,AddRef)  (THIS) IPURE;               \
    MAPIMETHOD_(ULONG,Release) (THIS) IPURE;   \
 
```

## <a name="see-also"></a><span data-ttu-id="6e6ff-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e6ff-118">See also</span></span>



[<span data-ttu-id="6e6ff-119">Vue d’ensemble de l’interface et de l’objet MAPI</span><span class="sxs-lookup"><span data-stu-id="6e6ff-119">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

