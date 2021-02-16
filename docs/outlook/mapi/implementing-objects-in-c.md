---
title: Implémentation des objets dans C
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 24fc4d78-726d-40ff-bad2-25dc298bd51a
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6026e697cc31545bf7ef518fcbd33ea8db48af5d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414941"
---
# <a name="implementing-objects-in-c"></a><span data-ttu-id="4b01f-103">Implémentation des objets dans C</span><span class="sxs-lookup"><span data-stu-id="4b01f-103">Implementing objects in C</span></span>

<span data-ttu-id="4b01f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b01f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b01f-105">Les applications clientes et les fournisseurs de services écrits en C définissent des objets MAPI en créant une structure de données et un tableau de pointeurs de fonction ordonnés appelé tableau virtuel ou tableau virtuel.</span><span class="sxs-lookup"><span data-stu-id="4b01f-105">Client applications and service providers written in C define MAPI objects by creating a data structure and an array of ordered function pointers known as a virtual function table, or vtable.</span></span> <span data-ttu-id="4b01f-106">Un pointeur vers le vtable doit être le premier membre de la structure de données.</span><span class="sxs-lookup"><span data-stu-id="4b01f-106">A pointer to the vtable must be the first member of the data structure.</span></span>
  
<span data-ttu-id="4b01f-107">Dans le vtable lui-même, il existe un pointeur pour chaque méthode dans chaque interface prise en charge par l’objet.</span><span class="sxs-lookup"><span data-stu-id="4b01f-107">In the vtable itself, there is one pointer for every method in each interface supported by the object.</span></span> <span data-ttu-id="4b01f-108">L’ordre des pointeurs doit suivre l’ordre des méthodes dans la spécification d’interface publiée dans le fichier d’en-tête Mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="4b01f-108">The order of the pointers must follow the order of the methods in the interface specification published in the Mapidefs.h header file.</span></span> <span data-ttu-id="4b01f-109">Chaque pointeur de fonction dans le vtable est définie sur l’adresse de l’implémentation réelle de la méthode.</span><span class="sxs-lookup"><span data-stu-id="4b01f-109">Each function pointer in the vtable is set to the address of the actual implementation of the method.</span></span> <span data-ttu-id="4b01f-110">En C++, le compilateur définit automatiquement le vtable.</span><span class="sxs-lookup"><span data-stu-id="4b01f-110">In C++, the compiler automatically sets up the vtable.</span></span> <span data-ttu-id="4b01f-111">En C, ce n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="4b01f-111">In C, it does not.</span></span> 
  
<span data-ttu-id="4b01f-112">L’illustration suivante montre comment cela fonctionne.</span><span class="sxs-lookup"><span data-stu-id="4b01f-112">The following illustration shows how this works.</span></span> <span data-ttu-id="4b01f-113">La zone à l’extrême gauche représente un client qui doit utiliser un objet fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="4b01f-113">The box on the far left represents a client that needs to use a service provider object.</span></span> <span data-ttu-id="4b01f-114">Au cours de la session, le client obtient un pointeur vers l’objet, **lpObject**.</span><span class="sxs-lookup"><span data-stu-id="4b01f-114">Through the session, the client obtains a pointer to the object, **lpObject**.</span></span> <span data-ttu-id="4b01f-115">Le vtable apparaît en premier dans l’objet suivi des données et méthodes privées.</span><span class="sxs-lookup"><span data-stu-id="4b01f-115">The vtable appears first in the object followed by private data and methods.</span></span> <span data-ttu-id="4b01f-116">Le pointeur vtable pointe vers le vtable réel, qui contient des pointeurs vers chacune des implémentations des méthodes dans l’interface.</span><span class="sxs-lookup"><span data-stu-id="4b01f-116">The vtable pointer points to the actual vtable, which contains pointers to each of the implementations of the methods in the interface.</span></span> 
  
<span data-ttu-id="4b01f-117">**Implémentation d’objet**</span><span class="sxs-lookup"><span data-stu-id="4b01f-117">**Object implementation**</span></span>
  
<span data-ttu-id="4b01f-118">![Implémentation d’objet Implémentation](media/amapi_42.gif "d’objet")</span><span class="sxs-lookup"><span data-stu-id="4b01f-118">![Object implementation](media/amapi_42.gif "Object implementation")</span></span>
  
<span data-ttu-id="4b01f-119">L’exemple de code suivant montre comment un fournisseur de services C peut définir un objet d’état simple.</span><span class="sxs-lookup"><span data-stu-id="4b01f-119">The following code example shows how a C service provider can define a simple status object.</span></span> <span data-ttu-id="4b01f-120">Le premier membre est le pointeur vtable ; Le reste de l’objet est composé de membres de données.</span><span class="sxs-lookup"><span data-stu-id="4b01f-120">The first member is the vtable pointer; the rest of the object is made up of data members.</span></span> 
  
```C
typedef struct _MYSTATUSOBJECT
{
    const STATUS_Vtbl FAR *lpVtbl;
    ULONG              cRef;
    ANOTHEROBJ        *pObj;
    LPMAPIPROP         lpProp;
    LPFREEBUFFER       lpFreeBuf;
} MYSTATUSOBJECT, *LPMYSTATUSOBJ;
 
```

<span data-ttu-id="4b01f-121">Étant donné que cet objet est un objet d’état, le vtable inclut des pointeurs vers les implémentations de chacune des méthodes dans l’interface [IMAPIStatus : IMAPIProp,](imapistatusimapiprop.md) ainsi que des pointeurs vers les implémentations de chacune des méthodes dans les interfaces de base — **IUnknown** et **IMAPIProp**.</span><span class="sxs-lookup"><span data-stu-id="4b01f-121">Because this object is a status object, the vtable includes pointers to implementations of each of the methods in the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface, as well as pointers to implementations of each of the methods in the base interfaces — **IUnknown** and **IMAPIProp**.</span></span> <span data-ttu-id="4b01f-122">L’ordre des méthodes dans le vtable correspond à l’ordre spécifié tel que défini dans le fichier d’en-tête Mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="4b01f-122">The order of methods in the vtable matches the specified order as defined in the Mapidefs.h header file.</span></span>
  
```js
static const MYOBJECT_Vtbl vtblSTATUS =
{
    STATUS_QueryInterface,
    STATUS_AddRef,
    STATUS_Release,
    STATUS_GetLastError,
    STATUS_SaveChanges,
    STATUS_GetProps,
    STATUS_GetPropList,
    STATUS_OpenProperty,
    STATUS_SetProps,
    STATUS_DeleteProps,
    STATUS_CopyTo,
    STATUS_CopyProps,
    STATUS_GetNamesFromIDs,
    STATUS_GetIDsFromNames,
    STATUS_ValidateState,
    STATUS_SettingsDialog,
    STATUS_ChangePassword,
    STATUS_FlushQueues
};
 
```

<span data-ttu-id="4b01f-123">Les clients et fournisseurs de services écrits en C utilisent des objets indirectement via le vtable et ajoutent un pointeur d’objet comme premier paramètre dans chaque appel.</span><span class="sxs-lookup"><span data-stu-id="4b01f-123">Clients and service providers written in C use objects indirectly through the vtable and add an object pointer as the first parameter in every call.</span></span> <span data-ttu-id="4b01f-124">Chaque appel à une méthode d’interface MAPI nécessite un pointeur vers l’objet appelé comme premier paramètre.</span><span class="sxs-lookup"><span data-stu-id="4b01f-124">Every call to a MAPI interface method requires a pointer to the object being called as its first parameter.</span></span> <span data-ttu-id="4b01f-125">C++ définit un pointeur spécial  appelé pointeur à cet effet.</span><span class="sxs-lookup"><span data-stu-id="4b01f-125">C++ defines a special pointer known as the **this** pointer for this purpose.</span></span> <span data-ttu-id="4b01f-126">Le compilateur C++ ajoute implicitement ce **pointeur** en tant que premier paramètre à chaque appel de méthode.</span><span class="sxs-lookup"><span data-stu-id="4b01f-126">The C++ compiler implicitly adds the **this** pointer as the first parameter to every method call.</span></span> <span data-ttu-id="4b01f-127">En C, il n’existe pas de pointeur de ce type ; Il doit être ajouté explicitement.</span><span class="sxs-lookup"><span data-stu-id="4b01f-127">In C there is no such pointer; it must be explicitly added.</span></span> 
  
<span data-ttu-id="4b01f-128">Le code suivant montre comment un client peut appeler une instance de MYSTATUSOBJECT :</span><span class="sxs-lookup"><span data-stu-id="4b01f-128">The following code demonstrates how a client can make a call to an instance of MYSTATUSOBJECT:</span></span>
  
```C
lpMyObj->lpVtbl->ValidateState(lpMyObj, ulUIParam, ulFlags);
 
```

## <a name="see-also"></a><span data-ttu-id="4b01f-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b01f-129">See also</span></span>

- [<span data-ttu-id="4b01f-130">Mise en œuvre des objets MAPI</span><span class="sxs-lookup"><span data-stu-id="4b01f-130">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

