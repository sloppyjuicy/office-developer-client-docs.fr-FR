---
title: CONTAB_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 84251222-dac4-4f4d-97b9-aa0e2cd26c44
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a2a204f76b62c8c6bc6d8a4e793c936a0184dc65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424083"
---
# <a name="contab_entryid"></a><span data-ttu-id="0c682-103">CONTAB_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="0c682-103">CONTAB_ENTRYID</span></span>

  
  
<span data-ttu-id="0c682-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c682-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c682-105">Contient l’ID d’entrée du dossier contacts.</span><span class="sxs-lookup"><span data-stu-id="0c682-105">Contains the entry ID of the contacts folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0c682-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="0c682-106">Header file:</span></span>  <br/> |<span data-ttu-id="0c682-107">msomapiutil.h</span><span class="sxs-lookup"><span data-stu-id="0c682-107">msomapiutil.h</span></span>  <br/> |
   
```cpp
#pragma pack(4) 
typedef struct _contab_entryid
{
    BYTE abFlags[4];
    MAPIUID muid;
    ULONG ulVersion;
    ULONG ulType;
    ULONG ulIndex;
    ULONG cbeid;
    BYTE abeid[1];
}   CONTAB_ENTRYID, *LPCONTAB_ENTRYID;
#pragma pack() 
```

## <a name="members"></a><span data-ttu-id="0c682-108">Members</span><span class="sxs-lookup"><span data-stu-id="0c682-108">Members</span></span>

 <span data-ttu-id="0c682-109">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="0c682-109">**abFlags**</span></span>
  
> <span data-ttu-id="0c682-110">Masque de bits d’indicateurs qui fournit des informations décrivant l’objet.</span><span class="sxs-lookup"><span data-stu-id="0c682-110">A bitmask of flags that provides information describing the object.</span></span> <span data-ttu-id="0c682-111">Pour plus d’informations, voir la description du champ **abFlags** d’une structure [ENTRYID.](entryid.md)</span><span class="sxs-lookup"><span data-stu-id="0c682-111">For more information, see the description of the **abFlags** field of an [ENTRYID](entryid.md) structure.</span></span> 
    
 <span data-ttu-id="0c682-112">**muid**</span><span class="sxs-lookup"><span data-stu-id="0c682-112">**muid**</span></span>
  
> <span data-ttu-id="0c682-113">GUID qui identifie le fournisseur du magasin.</span><span class="sxs-lookup"><span data-stu-id="0c682-113">GUID that identifies the store provider.</span></span>
    
 <span data-ttu-id="0c682-114">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="0c682-114">**ulVersion**</span></span>
  
> <span data-ttu-id="0c682-115">Numéro de version de la structure **CONTAB_ENTRYID** de base.</span><span class="sxs-lookup"><span data-stu-id="0c682-115">The version number of the **CONTAB_ENTRYID** structure.</span></span> <span data-ttu-id="0c682-116">Doit être définie sur CONTAB_VERSION.</span><span class="sxs-lookup"><span data-stu-id="0c682-116">Must be set to CONTAB_VERSION.</span></span> 
    
 <span data-ttu-id="0c682-117">**ulType**</span><span class="sxs-lookup"><span data-stu-id="0c682-117">**ulType**</span></span>
  
> <span data-ttu-id="0c682-118">Unteger représentant le type d’ID d’entrée de contact.</span><span class="sxs-lookup"><span data-stu-id="0c682-118">An integer representing the contact entry ID type.</span></span> <span data-ttu-id="0c682-119">Elle doit avoir l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="0c682-119">It must be one of the following values:</span></span>
    
|<span data-ttu-id="0c682-120">**Name**</span><span class="sxs-lookup"><span data-stu-id="0c682-120">**Name**</span></span>|<span data-ttu-id="0c682-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="0c682-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0c682-122">CONTAB_USER</span><span class="sxs-lookup"><span data-stu-id="0c682-122">CONTAB_USER</span></span>  <br/> |<span data-ttu-id="0c682-123">Objet d’utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="0c682-123">A messaging user object.</span></span>  <br/> |
|<span data-ttu-id="0c682-124">CONTAB_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="0c682-124">CONTAB_DISTLIST</span></span>  <br/> |<span data-ttu-id="0c682-125">Un objet de liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="0c682-125">A distribution list object.</span></span>  <br/> |
   
 <span data-ttu-id="0c682-126">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="0c682-126">**ulIndex**</span></span>
  
> <span data-ttu-id="0c682-127">Index dans le sous-ensemble de propriétés de messagerie.</span><span class="sxs-lookup"><span data-stu-id="0c682-127">The index into the email property subset.</span></span>
    
 <span data-ttu-id="0c682-128">**cbeid**</span><span class="sxs-lookup"><span data-stu-id="0c682-128">**cbeid**</span></span>
  
> <span data-ttu-id="0c682-129">Taille de l’identificateur d’entrée du message contact associé à cette entrée dans le carnet d’adresses des contacts.</span><span class="sxs-lookup"><span data-stu-id="0c682-129">The size of the entry identifier of the Contact message associated with this entry in the Contacts Address Book.</span></span>
    
 <span data-ttu-id="0c682-130">**abeid**</span><span class="sxs-lookup"><span data-stu-id="0c682-130">**abeid**</span></span>
  
> <span data-ttu-id="0c682-131">Identificateur d’entrée du message contact associé à cette entrée dans le carnet d’adresses des contacts.</span><span class="sxs-lookup"><span data-stu-id="0c682-131">The entry identifier of the Contact message associated with this entry in the Contacts Address Book.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0c682-132">Remarques</span><span class="sxs-lookup"><span data-stu-id="0c682-132">Remarks</span></span>

<span data-ttu-id="0c682-133">Un carnet d’adresses de contacts est un carnet d’adresses qui contient tous les éléments de contact d’un dossier Contacts qui ont une adresse de messagerie ou un numéro de télécopie.</span><span class="sxs-lookup"><span data-stu-id="0c682-133">A Contacts Address Book is an Address Book that contains all the contact items in a Contacts folder that have either an email address or a fax number.</span></span> <span data-ttu-id="0c682-134">Chaque entrée d’un carnet d’adresses de contacts est associée à une adresse de messagerie ou à un numéro de télécopie.</span><span class="sxs-lookup"><span data-stu-id="0c682-134">Each entry in a Contacts Address Book is associated with either an email address or a fax number.</span></span> <span data-ttu-id="0c682-135">Étant donné qu’un élément de contact peut avoir jusqu’à trois adresses de messagerie et trois numéros de télécopie, un élément de contact peut être représenté par six entrées au plus dans le carnet d’adresses des contacts correspondant.</span><span class="sxs-lookup"><span data-stu-id="0c682-135">Since a contact item can have up to three email addresses and three fax numbers, a contact item can be represented by up to six entries in the corresponding Contacts Address Book.</span></span>
  
<span data-ttu-id="0c682-136">L’objectif d’un carnet d’adresses de contacts est de prendre en charge les utilisateurs qui adressent des messages électroniques à des contacts dans un dossier Contacts.</span><span class="sxs-lookup"><span data-stu-id="0c682-136">The purpose of a Contacts Address Book is to support users addressing email messages to contacts in a Contacts folder.</span></span> <span data-ttu-id="0c682-137">Le fournisseur de carnet d’adresses contacts que Microsoft Outlook 2010 et Microsoft Outlook 2013 prendre en charge est contab32.dll.</span><span class="sxs-lookup"><span data-stu-id="0c682-137">The Contacts Address Book provider that Microsoft Outlook 2010 and Microsoft Outlook 2013 support is contab32.dll.</span></span>
  
<span data-ttu-id="0c682-138">La **structure CONTAB_ENTRYID** prend en charge un sous-ensemble des informations présentes dans le message de contact MAPI sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="0c682-138">The **CONTAB_ENTRYID** structure supports a subset of the information that is present in the underlying MAPI Contact message.</span></span> <span data-ttu-id="0c682-139">Il identifie le message de contact associé à une entrée de carnet d’adresses de contacts particulière.</span><span class="sxs-lookup"><span data-stu-id="0c682-139">It identifies the Contact message that a particular Contacts Address Book entry is associated with.</span></span> 
  
<span data-ttu-id="0c682-140">Les **champs cbeid** et **abeid** ne sont valides que lorsque la valeur du champ **ulType** est définie sur CONTAB_DISTLIST ou CONTAB_USER.</span><span class="sxs-lookup"><span data-stu-id="0c682-140">The **cbeid** and **abeid** fields are only valid when the **ulType** field value is set to CONTAB_DISTLIST or CONTAB_USER.</span></span> <span data-ttu-id="0c682-141">Lorsque la valeur du champ **ulType** est définie sur CONTAB_ROOT, CONTAB_SUBROOT ou CONTAB_CONTAINER, la [structure](dir_entryid.md) DIR_ENTRYID doit être utilisée à la place.</span><span class="sxs-lookup"><span data-stu-id="0c682-141">When the **ulType** field value is set to CONTAB_ROOT, CONTAB_SUBROOT, or CONTAB_CONTAINER, the [DIR_ENTRYID](dir_entryid.md) structure should be used instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0c682-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c682-142">See also</span></span>



[<span data-ttu-id="0c682-143">DIR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="0c682-143">DIR_ENTRYID</span></span>](dir_entryid.md)


[<span data-ttu-id="0c682-144">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="0c682-144">MAPI Structures</span></span>](mapi-structures.md)

