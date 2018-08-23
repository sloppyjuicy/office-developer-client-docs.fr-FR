---
title: Implémentation d’objets MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b1ee2533-8077-4976-846b-d42d148bf8c6
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d65ccec0ab270a59252c8a3ae94bdeca839fa807
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582363"
---
# <a name="implementing-mapi-objects"></a><span data-ttu-id="5ff35-103">Implémentation d’objets MAPI</span><span class="sxs-lookup"><span data-stu-id="5ff35-103">Implementing MAPI Objects</span></span>

  
  
<span data-ttu-id="5ff35-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ff35-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ff35-105">Objets MAPI peuvent être implémentés à l’aide des classes C++ ou C des structures de données, en fonction du langage et l’API de définie un client ou fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="5ff35-105">MAPI objects can be implemented by using C++ classes or C data structures, depending on the language and the API set a client or service provider is using.</span></span> <span data-ttu-id="5ff35-106">Fournisseurs de services peuvent être écrites en C ou C++ avec l’interface de fournisseur de services MAPI ; les applications clientes peuvent également utiliser C ou C++.</span><span class="sxs-lookup"><span data-stu-id="5ff35-106">Service providers can be written in C or C++ with the MAPI service provider interface; client applications can also use C or C++.</span></span> <span data-ttu-id="5ff35-107">Si possible, clients et fournisseurs de services qui utilisent l’interface de programmation orientée objet utilisez C++.</span><span class="sxs-lookup"><span data-stu-id="5ff35-107">If possible, clients and service providers that use the object-oriented programming interface should use C++.</span></span> 
  
<span data-ttu-id="5ff35-108">C++ est le meilleur choix car MAPI est une technologie orientée objet et C++ prête plus facilement à un développement orienté objet.</span><span class="sxs-lookup"><span data-stu-id="5ff35-108">C++ is the preferred choice because MAPI is an object-oriented technology, and C++ lends itself more readily to object-oriented development.</span></span> <span data-ttu-id="5ff35-109">Le code qui en résulte est plus simple et plus simple, ce qui facilite la maintenance.</span><span class="sxs-lookup"><span data-stu-id="5ff35-109">The resulting code is simpler and more straightforward, making it easier to maintain.</span></span> <span data-ttu-id="5ff35-110">La documentation de MAPI s’adresse essentiellement aux développeurs C++ ; toutes les descriptions de syntaxe pour les méthodes d’interface MAPI dans cette référence sont en langage C++.</span><span class="sxs-lookup"><span data-stu-id="5ff35-110">The MAPI documentation is written primarily for C++ developers; all of the syntax descriptions for the MAPI interface methods in this Reference are in C++.</span></span>
  
<span data-ttu-id="5ff35-111">Développeurs peuvent utiliser Microsoft Visual Studio et les outils de développement tiers pour développer des solutions qui appellent MAPI.</span><span class="sxs-lookup"><span data-stu-id="5ff35-111">Developers can use Microsoft Visual Studio and third-party development tools to develop solutions that call MAPI.</span></span> <span data-ttu-id="5ff35-112">Notez que les développeurs doivent utiliser C ou C++ non managé, mais non gérés C++ pour écrire des solutions de MAPI.</span><span class="sxs-lookup"><span data-stu-id="5ff35-112">Note that developers should use C or unmanaged C++, but not managed C++ to write MAPI solutions.</span></span>
  
<span data-ttu-id="5ff35-113">Lorsqu’un objet MAPI est implémenté, un client ou fournisseur de services crée du code pour toutes les méthodes d’interface, le code pour les méthodes privées qui sont spécifiques à l’implémentation et le code pour prendre en charge les données membres privées pour maintenir les informations d’état.</span><span class="sxs-lookup"><span data-stu-id="5ff35-113">When a MAPI object is implemented, a client or service provider creates code for all of the interface methods, code for any private methods that are specific to the implementation, and code to support private data members for maintaining state information.</span></span> <span data-ttu-id="5ff35-114">Le code pour les méthodes d’interface doit respecter les spécifications publiées par MAPI qui documentent le comportement attendu.</span><span class="sxs-lookup"><span data-stu-id="5ff35-114">The code for the interface methods must follow the specifications published by MAPI that document expected behavior.</span></span> 
  
<span data-ttu-id="5ff35-115">Il existe de nombreuses macros dans le fichier d’en-tête Mapidefs.h et fichiers d’en-tête OLE clients et fournisseurs de services dans une langue peuvent utiliser pour leur permettre de leurs définitions d’objets MAPI.</span><span class="sxs-lookup"><span data-stu-id="5ff35-115">There are many macros in the Mapidefs.h header file and OLE header files that clients and service providers in either language can use to help them with their definitions of MAPI objects.</span></span> <span data-ttu-id="5ff35-116">Par exemple, il existe une macro pour définir les méthodes de chaque interface MAPI.</span><span class="sxs-lookup"><span data-stu-id="5ff35-116">For example, there is a macro to define the methods of each of the MAPI interfaces.</span></span> <span data-ttu-id="5ff35-117">La macro pour définir les méthodes de l’interface [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) apparaît dans Mapidefs.h comme suit :</span><span class="sxs-lookup"><span data-stu-id="5ff35-117">The macro to define the methods of the [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) interface appears in Mapidefs.h as follows:</span></span> 
  
```cpp
#define MAPI_IUNKNOWN_METHODS(IPURE)          \
    MAPIMETHOD(QueryInterface)                \
        (THIS_ REFIID riid, LPVOID FAR * ppvObj) IPURE;    \
    MAPIMETHOD_(ULONG,AddRef)  (THIS) IPURE;               \
    MAPIMETHOD_(ULONG,Release) (THIS) IPURE;   \
 
```

## <a name="see-also"></a><span data-ttu-id="5ff35-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ff35-118">See also</span></span>



[<span data-ttu-id="5ff35-119">Objet MAPI et vue d’ensemble de l’Interface</span><span class="sxs-lookup"><span data-stu-id="5ff35-119">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

