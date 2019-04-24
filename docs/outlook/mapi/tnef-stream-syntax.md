---
title: Syntaxe de flux TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1353d494-c266-4715-afe7-14543a1bbe1b
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 12d2a92ff80897456707c7ab8af8f704605c85d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339633"
---
# <a name="tnef-stream-syntax"></a><span data-ttu-id="450a6-103">Syntaxe de flux TNEF</span><span class="sxs-lookup"><span data-stu-id="450a6-103">TNEF Stream Syntax</span></span>

  
  
<span data-ttu-id="450a6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="450a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="450a6-105">Cette rubrique présente une bakus-Nauer comme la description de la syntaxe de flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="450a6-105">This topic presents a Bakus-Nauer like description of the TNEF stream syntax.</span></span> <span data-ttu-id="450a6-106">Dans cette description, les éléments autres que les terminaux qui ont une définition supplémentaire sont en italique.</span><span class="sxs-lookup"><span data-stu-id="450a6-106">In this description, nonterminal elements that have a further definition are in italics.</span></span> <span data-ttu-id="450a6-107">Les constantes et les éléments littéraux sont en gras.</span><span class="sxs-lookup"><span data-stu-id="450a6-107">Constants and literal items are in bold.</span></span> <span data-ttu-id="450a6-108">Les séquences d'éléments sont répertoriées dans l'ordre sur une seule ligne.</span><span class="sxs-lookup"><span data-stu-id="450a6-108">Sequences of elements are listed in order on a single line.</span></span> <span data-ttu-id="450a6-109">Par exemple, l'élément de _flux_ se compose de la constante **TNEF_SIGNATURE**, suivie d'une _clé_, suivie d'un _objet_.</span><span class="sxs-lookup"><span data-stu-id="450a6-109">For example, the  _Stream_ item consists of the constant **TNEF_SIGNATURE**, followed by a  _Key_, followed by an  _Object_.</span></span> <span data-ttu-id="450a6-110">Lorsqu'un élément a plus d'une implémentation possible, les alternatives sont répertoriées sur des lignes consécutives.</span><span class="sxs-lookup"><span data-stu-id="450a6-110">When an item has more than one possible implementation, the alternatives are listed on consecutive lines.</span></span> <span data-ttu-id="450a6-111">Par exemple, un _objet_ peut être constitué d'un _Message_Seq_, d'un _Message_Seq_ suivi d'un _Attach_Seq_ou simplement d'un _Attach_Seq_.</span><span class="sxs-lookup"><span data-stu-id="450a6-111">For example, an  _Object_ can consist of a  _Message_Seq_, a  _Message_Seq_ followed by an  _Attach_Seq_, or just an  _Attach_Seq_.</span></span>
  
 <span data-ttu-id="450a6-112">_TNEF_Stream:_</span><span class="sxs-lookup"><span data-stu-id="450a6-112">_TNEF_Stream:_</span></span>
  
> <span data-ttu-id="450a6-113">**TNEF_SIGNATURE** _Clé_ _Objet_</span><span class="sxs-lookup"><span data-stu-id="450a6-113">**TNEF_SIGNATURE** _Key_ _Object_</span></span>
    
 <span data-ttu-id="450a6-114">_Flèche_</span><span class="sxs-lookup"><span data-stu-id="450a6-114">_Key:_</span></span>
  
> <span data-ttu-id="450a6-115">un entier non signé 16 bits différent de zéro</span><span class="sxs-lookup"><span data-stu-id="450a6-115">a nonzero 16-bit unsigned integer</span></span>
    
<span data-ttu-id="450a6-116">Les transports activés par TNEF génèrent cette valeur avant d'utiliser l'implémentation TNEF pour générer un flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="450a6-116">TNEF enabled transports generate this value before using the TNEF implementation to generate a TNEF stream.</span></span>
  
 <span data-ttu-id="450a6-117">_Dessin_</span><span class="sxs-lookup"><span data-stu-id="450a6-117">_Object:_</span></span>
  
>  <span data-ttu-id="450a6-118">_Message_Seq Message_Seq Attach_Seq Attach_Seq_</span><span class="sxs-lookup"><span data-stu-id="450a6-118">_Message_Seq Message_Seq Attach_Seq Attach_Seq_</span></span>
    
 <span data-ttu-id="450a6-119">_Message_Seq:_</span><span class="sxs-lookup"><span data-stu-id="450a6-119">_Message_Seq:_</span></span>
  
>  <span data-ttu-id="450a6-120">_attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="450a6-120">_attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_</span></span>
    
 <span data-ttu-id="450a6-121">_attTnefVersion:_</span><span class="sxs-lookup"><span data-stu-id="450a6-121">_attTnefVersion:_</span></span>
  
> <span data-ttu-id="450a6-122">**LVL_MESSAGE attTnefVersion sizeof (ULONG)** total de contrôle **0x00010000**</span><span class="sxs-lookup"><span data-stu-id="450a6-122">**LVL_MESSAGE attTnefVersion sizeof(ULONG)** **0x00010000** checksum</span></span> 
    
 <span data-ttu-id="450a6-123">_attMessageClass:_</span><span class="sxs-lookup"><span data-stu-id="450a6-123">_attMessageClass:_</span></span>
  
> <span data-ttu-id="450a6-124">**LVL_MESSAGE attMessageClass** _msg_class_length msg_class_ checksum</span><span class="sxs-lookup"><span data-stu-id="450a6-124">**LVL_MESSAGE attMessageClass** _msg_class_length msg_class_ checksum</span></span> 
    
 <span data-ttu-id="450a6-125">_Msg_Attribute_Seq:_</span><span class="sxs-lookup"><span data-stu-id="450a6-125">_Msg_Attribute_Seq:_</span></span>
  
>  <span data-ttu-id="450a6-126">_Msg_Attribute Msg_Attribute Msg_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="450a6-126">_Msg_Attribute Msg_Attribute Msg_Attribute_Seq_</span></span>
    
 <span data-ttu-id="450a6-127">_Msg_Attribute:_</span><span class="sxs-lookup"><span data-stu-id="450a6-127">_Msg_Attribute:_</span></span>
  
> <span data-ttu-id="450a6-128">Attribut de longueur d'attribut **LVL_MESSAGE** attribute-length-Data checksum</span><span class="sxs-lookup"><span data-stu-id="450a6-128">**LVL_MESSAGE** attribute-ID attribute-length attribute-data checksum</span></span> 
    
<span data-ttu-id="450a6-129">Attribute-ID est l'un des identificateurs d'attribut TNEF, tels que **attSubject**.</span><span class="sxs-lookup"><span data-stu-id="450a6-129">Attribute-ID is one of the TNEF attribute identifiers, such as **attSubject**.</span></span> <span data-ttu-id="450a6-130">Attribute-length est la longueur en octets des données d'attribut.</span><span class="sxs-lookup"><span data-stu-id="450a6-130">Attribute-length is the length in bytes of the attribute data.</span></span> <span data-ttu-id="450a6-131">Attribute-Data est les données associées à l'attribut.</span><span class="sxs-lookup"><span data-stu-id="450a6-131">Attribute-data is the data associated with the attribute.</span></span>
  
 <span data-ttu-id="450a6-132">_Attach_Seq:_</span><span class="sxs-lookup"><span data-stu-id="450a6-132">_Attach_Seq:_</span></span>
  
>  <span data-ttu-id="450a6-133">_attRenddata attRenddata Att_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="450a6-133">_attRenddata attRenddata Att_Attribute_Seq_</span></span>
    
 <span data-ttu-id="450a6-134">_attRenddata:_</span><span class="sxs-lookup"><span data-stu-id="450a6-134">_attRenddata:_</span></span>
  
> <span data-ttu-id="450a6-135">**LVL_ATTACHMENT attRenddata** **sizeof (RENDDATA)** RENDDATA checksum</span><span class="sxs-lookup"><span data-stu-id="450a6-135">**LVL_ATTACHMENT attRenddata** **sizeof(RENDDATA)** renddata checksum</span></span> 
    
<span data-ttu-id="450a6-136">Renddata est les données associées à la structure **Renddata** qui contient les informations de rendu pour la pièce jointe correspondante.</span><span class="sxs-lookup"><span data-stu-id="450a6-136">Renddata is the data associated with the **RENDDATA** structure that contains the rendering information for the corresponding attachment.</span></span> <span data-ttu-id="450a6-137">La structure **RENDDATA** est définie dans le format TNEF. Fichier d'en-tête H.</span><span class="sxs-lookup"><span data-stu-id="450a6-137">The **RENDDATA** structure is defined in the TNEF.H header file.</span></span> 
  
 <span data-ttu-id="450a6-138">_Att_Attribute_Seq:_</span><span class="sxs-lookup"><span data-stu-id="450a6-138">_Att_Attribute_Seq:_</span></span>
  
>  <span data-ttu-id="450a6-139">_Att_Attribute Att_Attribute Att_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="450a6-139">_Att_Attribute Att_Attribute Att_Attribute_Seq_</span></span>
    
 <span data-ttu-id="450a6-140">_Att_Attribute:_</span><span class="sxs-lookup"><span data-stu-id="450a6-140">_Att_Attribute:_</span></span>
  
> <span data-ttu-id="450a6-141">Attribut de longueur d'attribut **LVL_ATTACHMENT** attribute-length-Data checksum</span><span class="sxs-lookup"><span data-stu-id="450a6-141">**LVL_ATTACHMENT** attribute-ID attribute-length attribute-data checksum</span></span> 
    
<span data-ttu-id="450a6-142">Attribute-ID, attribute-Length et attribute-Data ont les mêmes significations que pour l'élément Msg_Attribute.</span><span class="sxs-lookup"><span data-stu-id="450a6-142">Attribute-ID, attribute-length, and attribute-data have the same meanings as for the Msg_Attribute item.</span></span>
  

