---
title: Implémentation d’objets dans C
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 24fc4d78-726d-40ff-bad2-25dc298bd51a
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d07d756abded137d3268daf7dd0998f0c953cb1d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563946"
---
# <a name="implementing-objects-in-c"></a><span data-ttu-id="1ff5a-103">Implémentation d’objets dans C</span><span class="sxs-lookup"><span data-stu-id="1ff5a-103">Implementing objects in C</span></span>

<span data-ttu-id="1ff5a-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ff5a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ff5a-105">Applications clientes et des fournisseurs de services écrits en C définissent les objets MAPI en créant une structure de données et un tableau de pointeurs fonction triée appelé une table de fonctions virtuelles ou vtable.</span><span class="sxs-lookup"><span data-stu-id="1ff5a-105">Client applications and service providers written in C define MAPI objects by creating a data structure and an array of ordered function pointers known as a virtual function table, or vtable.</span></span> <span data-ttu-id="1ff5a-106">Un pointeur vers la vtable doit être le premier membre de la structure de données.</span><span class="sxs-lookup"><span data-stu-id="1ff5a-106">A pointer to the vtable must be the first member of the data structure.</span></span>
  
<span data-ttu-id="1ff5a-107">Dans la vtable lui-même, il existe un pointeur pour chaque méthode dans chaque interface pris en charge par l’objet.</span><span class="sxs-lookup"><span data-stu-id="1ff5a-107">In the vtable itself, there is one pointer for every method in each interface supported by the object.</span></span> <span data-ttu-id="1ff5a-108">L’ordre des pointeurs doit respecter l’ordre des méthodes de l’interface publiée dans le fichier d’en-tête Mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="1ff5a-108">The order of the pointers must follow the order of the methods in the interface specification published in the Mapidefs.h header file.</span></span> <span data-ttu-id="1ff5a-109">Chaque pointeur de fonction vtable est définie à l’adresse de l’implémentation de la méthode réelle.</span><span class="sxs-lookup"><span data-stu-id="1ff5a-109">Each function pointer in the vtable is set to the address of the actual implementation of the method.</span></span> <span data-ttu-id="1ff5a-110">En C++, le compilateur définit automatiquement la vtable.</span><span class="sxs-lookup"><span data-stu-id="1ff5a-110">In C++, the compiler automatically sets up the vtable.</span></span> <span data-ttu-id="1ff5a-111">C, il n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="1ff5a-111">In C, it does not.</span></span> 
  
<span data-ttu-id="1ff5a-112">L’illustration suivante montre comment cela fonctionne.</span><span class="sxs-lookup"><span data-stu-id="1ff5a-112">The following illustration shows how this works.</span></span> <span data-ttu-id="1ff5a-113">La zone à l’extrême gauche représente un client qui a besoin d’utiliser un objet de fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="1ff5a-113">The box on the far left represents a client that needs to use a service provider object.</span></span> <span data-ttu-id="1ff5a-114">Par le biais de la session, le client obtient un pointeur vers l’objet, **lpObject**.</span><span class="sxs-lookup"><span data-stu-id="1ff5a-114">Through the session, the client obtains a pointer to the object, **lpObject**.</span></span> <span data-ttu-id="1ff5a-115">Vtable apparaît en premier dans l’objet suivi par des méthodes et des données privées.</span><span class="sxs-lookup"><span data-stu-id="1ff5a-115">The vtable appears first in the object followed by private data and methods.</span></span> <span data-ttu-id="1ff5a-116">Le pointeur vtable pointe vers la vtable réelle, qui contient des pointeurs à chacun des implémentations des méthodes dans l’interface.</span><span class="sxs-lookup"><span data-stu-id="1ff5a-116">The vtable pointer points to the actual vtable, which contains pointers to each of the implementations of the methods in the interface.</span></span> 
  
<span data-ttu-id="1ff5a-117">**Implémentation d’objet**</span><span class="sxs-lookup"><span data-stu-id="1ff5a-117">**Object implementation**</span></span>
  
<span data-ttu-id="1ff5a-118">![Implémentation de l’objet] (media/amapi_42.gif "Implémentation de l’objet")</span><span class="sxs-lookup"><span data-stu-id="1ff5a-118">![Object implementation](media/amapi_42.gif "Object implementation")</span></span>
  
<span data-ttu-id="1ff5a-119">L’exemple de code suivant montre comment un fournisseur de services C définir un objet état simple.</span><span class="sxs-lookup"><span data-stu-id="1ff5a-119">The following code example shows how a C service provider can define a simple status object.</span></span> <span data-ttu-id="1ff5a-120">Le premier membre est le pointeur vtable ; le reste de l’objet est composé des membres de données.</span><span class="sxs-lookup"><span data-stu-id="1ff5a-120">The first member is the vtable pointer; the rest of the object is made up of data members.</span></span> 
  
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

<span data-ttu-id="1ff5a-121">Étant donné que cet objet est un objet d’état, vtable comprend des pointeurs vers des implémentations de chacune des méthodes dans le [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface, ainsi que des pointeurs vers des implémentations de chacune des méthodes dans les interfaces de base — **IUnknown **et **IMAPIProp**.</span><span class="sxs-lookup"><span data-stu-id="1ff5a-121">Because this object is a status object, the vtable includes pointers to implementations of each of the methods in the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface, as well as pointers to implementations of each of the methods in the base interfaces — **IUnknown** and **IMAPIProp**.</span></span> <span data-ttu-id="1ff5a-122">L’ordre des méthodes vtable correspond à l’ordre spécifié comme défini dans le fichier d’en-tête Mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="1ff5a-122">The order of methods in the vtable matches the specified order as defined in the Mapidefs.h header file.</span></span>
  
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

<span data-ttu-id="1ff5a-123">Clients et fournisseurs de services écrits en C des objets indirectement via la vtable et ajoutez un pointeur d’objet en tant que le premier paramètre de chaque appel.</span><span class="sxs-lookup"><span data-stu-id="1ff5a-123">Clients and service providers written in C use objects indirectly through the vtable and add an object pointer as the first parameter in every call.</span></span> <span data-ttu-id="1ff5a-124">Chaque appel à une méthode d’interface MAPI nécessite un pointeur vers l’objet appelé comme premier paramètre.</span><span class="sxs-lookup"><span data-stu-id="1ff5a-124">Every call to a MAPI interface method requires a pointer to the object being called as its first parameter.</span></span> <span data-ttu-id="1ff5a-125">C++ définit un pointeur spécial appelé le pointeur **this** à cet effet.</span><span class="sxs-lookup"><span data-stu-id="1ff5a-125">C++ defines a special pointer known as the **this** pointer for this purpose.</span></span> <span data-ttu-id="1ff5a-126">Le compilateur C++ ajoute implicitement le pointeur **this** comme premier paramètre à chaque appel de méthode.</span><span class="sxs-lookup"><span data-stu-id="1ff5a-126">The C++ compiler implicitly adds the **this** pointer as the first parameter to every method call.</span></span> <span data-ttu-id="1ff5a-127">C il n’existe aucun pointeur de ce type ; Il doit être explicitement ajoutée.</span><span class="sxs-lookup"><span data-stu-id="1ff5a-127">In C there is no such pointer; it must be explicitly added.</span></span> 
  
<span data-ttu-id="1ff5a-128">Le code suivant montre comment un client peut effectuer un appel à une instance de MYSTATUSOBJECT :</span><span class="sxs-lookup"><span data-stu-id="1ff5a-128">The following code demonstrates how a client can make a call to an instance of MYSTATUSOBJECT:</span></span>
  
```C
lpMyObj->lpVtbl->ValidateState(lpMyObj, ulUIParam, ulFlags);
 
```

## <a name="see-also"></a><span data-ttu-id="1ff5a-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ff5a-129">See also</span></span>

- [<span data-ttu-id="1ff5a-130">Implémentation d’objets MAPI</span><span class="sxs-lookup"><span data-stu-id="1ff5a-130">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

