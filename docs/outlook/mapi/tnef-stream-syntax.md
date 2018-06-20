---
title: Syntaxe de flux TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1353d494-c266-4715-afe7-14543a1bbe1b
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: cbaf37415608dd1d79a06be65b34632f2b4afc89
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787379"
---
# <a name="tnef-stream-syntax"></a><span data-ttu-id="997d8-103">Syntaxe de flux TNEF</span><span class="sxs-lookup"><span data-stu-id="997d8-103">TNEF Stream Syntax</span></span>

  
  
<span data-ttu-id="997d8-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="997d8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="997d8-105">Cette rubrique présente un Bakus-Nauer comme description de la syntaxe de flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="997d8-105">This topic presents a Bakus-Nauer like description of the TNEF stream syntax.</span></span> <span data-ttu-id="997d8-106">Dans cette description, les éléments non terminaux possédant une définition plus précise sont en italique.</span><span class="sxs-lookup"><span data-stu-id="997d8-106">In this description, nonterminal elements that have a further definition are in italics.</span></span> <span data-ttu-id="997d8-107">Constantes et éléments littérales sont en gras.</span><span class="sxs-lookup"><span data-stu-id="997d8-107">Constants and literal items are in bold.</span></span> <span data-ttu-id="997d8-108">Séquences d’éléments sont répertoriés dans l’ordre sur une seule ligne.</span><span class="sxs-lookup"><span data-stu-id="997d8-108">Sequences of elements are listed in order on a single line.</span></span> <span data-ttu-id="997d8-109">Par exemple, l’élément de _flux de données_ se compose de la constante **TNEF_SIGNATURE**, suivi d’une _clé_, suivi d’un _objet_.</span><span class="sxs-lookup"><span data-stu-id="997d8-109">For example, the  _Stream_ item consists of the constant **TNEF_SIGNATURE**, followed by a  _Key_, followed by an  _Object_.</span></span> <span data-ttu-id="997d8-110">Lorsqu’un élément a plus d’une implémentation possible, les alternatives figurent sur des lignes consécutives.</span><span class="sxs-lookup"><span data-stu-id="997d8-110">When an item has more than one possible implementation, the alternatives are listed on consecutive lines.</span></span> <span data-ttu-id="997d8-111">Par exemple, un _objet_ peut se composer d’un _Message_Seq_, un _Message_Seq_ suivi d’un _Attach_Seq_ou juste un _Attach_Seq_.</span><span class="sxs-lookup"><span data-stu-id="997d8-111">For example, an  _Object_ can consist of a  _Message_Seq_, a  _Message_Seq_ followed by an  _Attach_Seq_, or just an  _Attach_Seq_.</span></span>
  
 <span data-ttu-id="997d8-112">_TNEF_Stream :_</span><span class="sxs-lookup"><span data-stu-id="997d8-112">_TNEF_Stream:_</span></span>
  
> <span data-ttu-id="997d8-113">**TNEF_SIGNATURE** _Clé_ _Objet_</span><span class="sxs-lookup"><span data-stu-id="997d8-113">**TNEF_SIGNATURE** _Key_ _Object_</span></span>
    
 <span data-ttu-id="997d8-114">_Clé :_</span><span class="sxs-lookup"><span data-stu-id="997d8-114">_Key:_</span></span>
  
> <span data-ttu-id="997d8-115">un entier non signé de 16 bits différente de zéro</span><span class="sxs-lookup"><span data-stu-id="997d8-115">a nonzero 16-bit unsigned integer</span></span>
    
<span data-ttu-id="997d8-116">Transports TNEF activé génèrent cette valeur avant d’utiliser la mise en œuvre TNEF pour générer un flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="997d8-116">TNEF enabled transports generate this value before using the TNEF implementation to generate a TNEF stream.</span></span>
  
 <span data-ttu-id="997d8-117">_Objet :_</span><span class="sxs-lookup"><span data-stu-id="997d8-117">_Object:_</span></span>
  
>  <span data-ttu-id="997d8-118">_Message_Seq Message_Seq Attach_Seq Attach_Seq_</span><span class="sxs-lookup"><span data-stu-id="997d8-118">_Message_Seq Message_Seq Attach_Seq Attach_Seq_</span></span>
    
 <span data-ttu-id="997d8-119">_Message_Seq :_</span><span class="sxs-lookup"><span data-stu-id="997d8-119">_Message_Seq:_</span></span>
  
>  <span data-ttu-id="997d8-120">_attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="997d8-120">_attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_</span></span>
    
 <span data-ttu-id="997d8-121">_attTnefVersion :_</span><span class="sxs-lookup"><span data-stu-id="997d8-121">_attTnefVersion:_</span></span>
  
> <span data-ttu-id="997d8-122">**LVL_MESSAGE attTnefVersion sizeof** **0 x 00010000** somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="997d8-122">**LVL_MESSAGE attTnefVersion sizeof(ULONG)** **0x00010000** checksum</span></span> 
    
 <span data-ttu-id="997d8-123">_attMessageClass :_</span><span class="sxs-lookup"><span data-stu-id="997d8-123">_attMessageClass:_</span></span>
  
> <span data-ttu-id="997d8-124">**LVL_MESSAGE attMessageClass** somme de contrôle _msg_class_length msg_class_</span><span class="sxs-lookup"><span data-stu-id="997d8-124">**LVL_MESSAGE attMessageClass** _msg_class_length msg_class_ checksum</span></span> 
    
 <span data-ttu-id="997d8-125">_Msg_Attribute_Seq :_</span><span class="sxs-lookup"><span data-stu-id="997d8-125">_Msg_Attribute_Seq:_</span></span>
  
>  <span data-ttu-id="997d8-126">_Msg_Attribute Msg_Attribute Msg_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="997d8-126">_Msg_Attribute Msg_Attribute Msg_Attribute_Seq_</span></span>
    
 <span data-ttu-id="997d8-127">_Msg_Attribute :_</span><span class="sxs-lookup"><span data-stu-id="997d8-127">_Msg_Attribute:_</span></span>
  
> <span data-ttu-id="997d8-128">Somme de contrôle **LVL_MESSAGE** -ID de l’attribut attribut longueur données d’attribut</span><span class="sxs-lookup"><span data-stu-id="997d8-128">**LVL_MESSAGE** attribute-ID attribute-length attribute-data checksum</span></span> 
    
<span data-ttu-id="997d8-129">Attribut-ID est un des identificateurs d’attribut TNEF, tel que **attSubject**.</span><span class="sxs-lookup"><span data-stu-id="997d8-129">Attribute-ID is one of the TNEF attribute identifiers, such as **attSubject**.</span></span> <span data-ttu-id="997d8-130">Longueur de l’attribut est la longueur, en octets, des données d’attribut.</span><span class="sxs-lookup"><span data-stu-id="997d8-130">Attribute-length is the length in bytes of the attribute data.</span></span> <span data-ttu-id="997d8-131">Données d’attribut sont les données associées à l’attribut.</span><span class="sxs-lookup"><span data-stu-id="997d8-131">Attribute-data is the data associated with the attribute.</span></span>
  
 <span data-ttu-id="997d8-132">_Attach_Seq :_</span><span class="sxs-lookup"><span data-stu-id="997d8-132">_Attach_Seq:_</span></span>
  
>  <span data-ttu-id="997d8-133">_attRenddata attRenddata Att_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="997d8-133">_attRenddata attRenddata Att_Attribute_Seq_</span></span>
    
 <span data-ttu-id="997d8-134">_attRenddata :_</span><span class="sxs-lookup"><span data-stu-id="997d8-134">_attRenddata:_</span></span>
  
> <span data-ttu-id="997d8-135">**LVL_ATTACHMENT attRenddata** somme de contrôle **sizeof(RENDDATA)** renddata</span><span class="sxs-lookup"><span data-stu-id="997d8-135">**LVL_ATTACHMENT attRenddata** **sizeof(RENDDATA)** renddata checksum</span></span> 
    
<span data-ttu-id="997d8-136">Renddata est les données associées à la structure **RENDDATA** qui contient les informations de rendu de la pièce jointe correspondante.</span><span class="sxs-lookup"><span data-stu-id="997d8-136">Renddata is the data associated with the **RENDDATA** structure that contains the rendering information for the corresponding attachment.</span></span> <span data-ttu-id="997d8-137">La structure **RENDDATA** est définie dans le format TNEF. Fichier d’en-tête H.</span><span class="sxs-lookup"><span data-stu-id="997d8-137">The **RENDDATA** structure is defined in the TNEF.H header file.</span></span> 
  
 <span data-ttu-id="997d8-138">_Att_Attribute_Seq :_</span><span class="sxs-lookup"><span data-stu-id="997d8-138">_Att_Attribute_Seq:_</span></span>
  
>  <span data-ttu-id="997d8-139">_Att_Attribute Att_Attribute Att_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="997d8-139">_Att_Attribute Att_Attribute Att_Attribute_Seq_</span></span>
    
 <span data-ttu-id="997d8-140">_Att_Attribute :_</span><span class="sxs-lookup"><span data-stu-id="997d8-140">_Att_Attribute:_</span></span>
  
> <span data-ttu-id="997d8-141">Somme de contrôle **LVL_ATTACHMENT** -ID de l’attribut attribut longueur données d’attribut</span><span class="sxs-lookup"><span data-stu-id="997d8-141">**LVL_ATTACHMENT** attribute-ID attribute-length attribute-data checksum</span></span> 
    
<span data-ttu-id="997d8-142">ID d’attribut, longueur de l’attribut et données d’attribut ont la même signification que pour l’élément Msg_Attribute.</span><span class="sxs-lookup"><span data-stu-id="997d8-142">Attribute-ID, attribute-length, and attribute-data have the same meanings as for the Msg_Attribute item.</span></span>
  

