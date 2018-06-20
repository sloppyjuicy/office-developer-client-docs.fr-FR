---
title: CONTAB_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 84251222-dac4-4f4d-97b9-aa0e2cd26c44
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 2c8661f24ed9555547446cf63fc08a3be7e6e941
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783059"
---
# <a name="contabentryid"></a><span data-ttu-id="24dc3-103">CONTAB_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="24dc3-103">CONTAB_ENTRYID</span></span>

  
  
<span data-ttu-id="24dc3-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="24dc3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="24dc3-105">Contient l’identificateur d’entrée du dossier contacts.</span><span class="sxs-lookup"><span data-stu-id="24dc3-105">Contains the entry ID of the contacts folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="24dc3-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="24dc3-106">Header file:</span></span>  <br/> |<span data-ttu-id="24dc3-107">msomapiutil.h</span><span class="sxs-lookup"><span data-stu-id="24dc3-107">msomapiutil.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="24dc3-108">Membres</span><span class="sxs-lookup"><span data-stu-id="24dc3-108">Members</span></span>

 <span data-ttu-id="24dc3-109">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="24dc3-109">**abFlags**</span></span>
  
> <span data-ttu-id="24dc3-110">Masque de bits d’indicateurs qui fournit des informations décrivant l’objet.</span><span class="sxs-lookup"><span data-stu-id="24dc3-110">A bitmask of flags that provides information describing the object.</span></span> <span data-ttu-id="24dc3-111">Pour plus d’informations, voir la description du champ **abFlags** d’une structure [ENTRYID](entryid.md) .</span><span class="sxs-lookup"><span data-stu-id="24dc3-111">For more information, see the description of the **abFlags** field of an [ENTRYID](entryid.md) structure.</span></span> 
    
 <span data-ttu-id="24dc3-112">**muid**</span><span class="sxs-lookup"><span data-stu-id="24dc3-112">**muid**</span></span>
  
> <span data-ttu-id="24dc3-113">GUID qui identifie le fournisseur de banque.</span><span class="sxs-lookup"><span data-stu-id="24dc3-113">GUID that identifies the store provider.</span></span>
    
 <span data-ttu-id="24dc3-114">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="24dc3-114">**ulVersion**</span></span>
  
> <span data-ttu-id="24dc3-115">Le numéro de version de la structure **CONTAB_ENTRYID** .</span><span class="sxs-lookup"><span data-stu-id="24dc3-115">The version number of the **CONTAB_ENTRYID** structure.</span></span> <span data-ttu-id="24dc3-116">Doit être défini sur CONTAB_VERSION.</span><span class="sxs-lookup"><span data-stu-id="24dc3-116">Must be set to CONTAB_VERSION.</span></span> 
    
 <span data-ttu-id="24dc3-117">**ulType**</span><span class="sxs-lookup"><span data-stu-id="24dc3-117">**ulType**</span></span>
  
> <span data-ttu-id="24dc3-118">Nombre entier représentant le type d’ID entrée du contact.</span><span class="sxs-lookup"><span data-stu-id="24dc3-118">An integer representing the contact entry ID type.</span></span> <span data-ttu-id="24dc3-119">Il doit être une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="24dc3-119">It must be one of the following values:</span></span>
    
|<span data-ttu-id="24dc3-120">**Nom**</span><span class="sxs-lookup"><span data-stu-id="24dc3-120">**Name**</span></span>|<span data-ttu-id="24dc3-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="24dc3-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="24dc3-122">CONTAB_USER</span><span class="sxs-lookup"><span data-stu-id="24dc3-122">CONTAB_USER</span></span>  <br/> |<span data-ttu-id="24dc3-123">Un objet utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="24dc3-123">A messaging user object.</span></span>  <br/> |
|<span data-ttu-id="24dc3-124">CONTAB_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="24dc3-124">CONTAB_DISTLIST</span></span>  <br/> |<span data-ttu-id="24dc3-125">Un objet de liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="24dc3-125">A distribution list object.</span></span>  <br/> |
   
 <span data-ttu-id="24dc3-126">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="24dc3-126">**ulIndex**</span></span>
  
> <span data-ttu-id="24dc3-127">L’index dans le sous-ensemble de propriété de messagerie.</span><span class="sxs-lookup"><span data-stu-id="24dc3-127">The index into the email property subset.</span></span>
    
 <span data-ttu-id="24dc3-128">**cbeid**</span><span class="sxs-lookup"><span data-stu-id="24dc3-128">**cbeid**</span></span>
  
> <span data-ttu-id="24dc3-129">La taille de l’identificateur d’entrée du message Contact associé à cette entrée dans le carnet d’adresses de Contacts.</span><span class="sxs-lookup"><span data-stu-id="24dc3-129">The size of the entry identifier of the Contact message associated with this entry in the Contacts Address Book.</span></span>
    
 <span data-ttu-id="24dc3-130">**abeid**</span><span class="sxs-lookup"><span data-stu-id="24dc3-130">**abeid**</span></span>
  
> <span data-ttu-id="24dc3-131">L’identificateur d’entrée du message Contact associé à cette entrée dans le carnet d’adresses de Contacts.</span><span class="sxs-lookup"><span data-stu-id="24dc3-131">The entry identifier of the Contact message associated with this entry in the Contacts Address Book.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="24dc3-132">Remarques</span><span class="sxs-lookup"><span data-stu-id="24dc3-132">Remarks</span></span>

<span data-ttu-id="24dc3-133">Un carnet d’adresses de Contacts est un carnet d’adresses qui contient tous les éléments Contacts dans un dossier Contacts qui possèdent une adresse de messagerie ou un numéro de télécopie.</span><span class="sxs-lookup"><span data-stu-id="24dc3-133">A Contacts Address Book is an Address Book that contains all the contact items in a Contacts folder that have either an email address or a fax number.</span></span> <span data-ttu-id="24dc3-134">Chaque entrée dans un carnet d’adresses de Contacts est associée à une adresse électronique ou un numéro de télécopie.</span><span class="sxs-lookup"><span data-stu-id="24dc3-134">Each entry in a Contacts Address Book is associated with either an email address or a fax number.</span></span> <span data-ttu-id="24dc3-135">Dans la mesure où un élément de contact peut avoir jusqu'à trois adresses de messagerie et trois numéros de télécopie, un élément de contact peut être représenté par jusqu'à six entrées dans le carnet d’adresses de Contacts correspondant.</span><span class="sxs-lookup"><span data-stu-id="24dc3-135">Since a contact item can have up to three email addresses and three fax numbers, a contact item can be represented by up to six entries in the corresponding Contacts Address Book.</span></span>
  
<span data-ttu-id="24dc3-136">L’objectif d’un carnet d’adresses de Contacts consiste à prendre en charge les utilisateurs de l’adressage des messages électroniques aux contacts d’un dossier Contacts.</span><span class="sxs-lookup"><span data-stu-id="24dc3-136">The purpose of a Contacts Address Book is to support users addressing email messages to contacts in a Contacts folder.</span></span> <span data-ttu-id="24dc3-137">Le fournisseur de carnet d’adresses de Contacts qui prennent en charge de Microsoft Outlook 2010 et Microsoft Outlook 2013 est contab32.dll.</span><span class="sxs-lookup"><span data-stu-id="24dc3-137">The Contacts Address Book provider that Microsoft Outlook 2010 and Microsoft Outlook 2013 support is contab32.dll.</span></span>
  
<span data-ttu-id="24dc3-138">La structure **CONTAB_ENTRYID** prend en charge un sous-ensemble des informations qui se trouve dans le message MAPI Contact sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="24dc3-138">The **CONTAB_ENTRYID** structure supports a subset of the information that is present in the underlying MAPI Contact message.</span></span> <span data-ttu-id="24dc3-139">Il identifie le message de Contact qui est associée à une entrée de carnet d’adresses de Contacts particulier.</span><span class="sxs-lookup"><span data-stu-id="24dc3-139">It identifies the Contact message that a particular Contacts Address Book entry is associated with.</span></span> 
  
<span data-ttu-id="24dc3-140">Les champs **cbeid** et **abeid** ne sont valides que lorsque la valeur du champ **ulType** est définie sur CONTAB_DISTLIST ou CONTAB_USER.</span><span class="sxs-lookup"><span data-stu-id="24dc3-140">The **cbeid** and **abeid** fields are only valid when the **ulType** field value is set to CONTAB_DISTLIST or CONTAB_USER.</span></span> <span data-ttu-id="24dc3-141">Lorsque la valeur du champ **ulType** est définie sur CONTAB_ROOT, CONTAB_SUBROOT ou CONTAB_CONTAINER, la structure [DIR_ENTRYID](dir_entryid.md) doit être utilisée à la place.</span><span class="sxs-lookup"><span data-stu-id="24dc3-141">When the **ulType** field value is set to CONTAB_ROOT, CONTAB_SUBROOT, or CONTAB_CONTAINER, the [DIR_ENTRYID](dir_entryid.md) structure should be used instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="24dc3-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24dc3-142">See also</span></span>



[<span data-ttu-id="24dc3-143">DIR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="24dc3-143">DIR_ENTRYID</span></span>](dir_entryid.md)


[<span data-ttu-id="24dc3-144">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="24dc3-144">MAPI Structures</span></span>](mapi-structures.md)

