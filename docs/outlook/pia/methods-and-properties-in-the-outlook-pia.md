---
title: Méthodes et propriétés dans l'assembly PIA Outlook
TOCTitle: Methods and properties in the Outlook PIA
ms:assetid: ec7742de-ead6-41dd-90a3-1280fdf09d54
ms:mtpsurl: https://msdn.microsoft.com/library/Bb612528(v=office.15)
ms:contentKeyID: 55119780
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 90c13559094fbffd2dbe9a99602ee235c92d9445
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351032"
---
# <a name="methods-and-properties-in-the-outlook-pia"></a><span data-ttu-id="70590-102">Méthodes et propriétés dans l'assembly PIA Outlook</span><span class="sxs-lookup"><span data-stu-id="70590-102">Methods and properties in the Outlook PIA</span></span>

<span data-ttu-id="70590-103">Cette rubrique décrit comment accéder aux méthodes et propriétés d’un objet dans le code managé à l’aide de l'assembly PIA Outlook (Primary Interop Assembly).</span><span class="sxs-lookup"><span data-stu-id="70590-103">This topic describes how to access methods and properties of an object in managed code by using the Outlook Primary Interop Assembly (PIA).</span></span>

## <a name="where-helper-objects-come-from"></a><span data-ttu-id="70590-104">D'où viennent les objets d'assistance ?</span><span class="sxs-lookup"><span data-stu-id="70590-104">Where Helper objects come from</span></span>

<span data-ttu-id="70590-p101">Pour créer l'assembly PIA Outlook, Outlook utilise l'outil Type Library Importer (TLBIMP) de .NET Framework pour convertir les définitions de types de la bibliothèque de types COM en définitions équivalentes dans un assembly CLR (Common Language Runtime). Dans COM, un objet est une coclasse formée des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="70590-p101">To create the Outlook PIA, Outlook uses the Type Library Importer (TLBIMP) in the .NET Framework to convert type definitions in the COM type library into equivalent definitions in a common language runtime (CLR) assembly. In COM, an object is actually a coclass that consists of the following:</span></span>

- <span data-ttu-id="70590-107">L'interface principale (par exemple l'interface [\_FormRegion](https://msdn.microsoft.com/library/bb645761\(v=office.15\))).</span><span class="sxs-lookup"><span data-stu-id="70590-107">The primary interface (for example, the [\_FormRegion](https://msdn.microsoft.com/library/bb645761\(v=office.15\)) interface).</span></span>

- <span data-ttu-id="70590-108">L'interface d'événement (par exemple l'interface [FormRegionEvents](https://msdn.microsoft.com/library/bb611940\(v=office.15\))).</span><span class="sxs-lookup"><span data-stu-id="70590-108">The event interface (for example, the [FormRegionEvents](https://msdn.microsoft.com/library/bb611940\(v=office.15\)) interface).</span></span>

<span data-ttu-id="70590-109">L'outil TLBIMP importe l'interface principale et l'interface d'événement pour chaque objet et crée un certain nombre d'interfaces, de délégués et de classes, dont les suivants :</span><span class="sxs-lookup"><span data-stu-id="70590-109">TLBIMP imports the primary interface and the event interface for each object and creates a number of interfaces, delegates, and classes, among which are the following:</span></span>

- <span data-ttu-id="70590-110">L'interface d'événement .NET (par exemple l'interface [FormRegionEvents\_Event](https://msdn.microsoft.com/library/bb647619\(v=office.15\))).</span><span class="sxs-lookup"><span data-stu-id="70590-110">The .NET event interface (for example, the [FormRegionEvents\_Event](https://msdn.microsoft.com/library/bb647619\(v=office.15\)) interface).</span></span>

- <span data-ttu-id="70590-111">La classe .NET (par exemple, la classe [FormRegionClass](https://msdn.microsoft.com/library/bb624204\(v=office.15\))).</span><span class="sxs-lookup"><span data-stu-id="70590-111">The .NET class (for example, the [FormRegionClass](https://msdn.microsoft.com/library/bb624204\(v=office.15\)) class).</span></span>

- <span data-ttu-id="70590-112">L'interface .NET principale (par exemple l'interface [FormRegion](https://msdn.microsoft.com/library/bb652633\(v=office.15\))).</span><span class="sxs-lookup"><span data-stu-id="70590-112">The .NET interface (for example, the [FormRegion](https://msdn.microsoft.com/library/bb652633\(v=office.15\)) interface).</span></span>

## <a name="what-the-helper-objects-are-for"></a><span data-ttu-id="70590-113">À quoi servent les objets d'assistance ?</span><span class="sxs-lookup"><span data-stu-id="70590-113">What the Helper objects are for</span></span>

<span data-ttu-id="70590-114">En continuant à utiliser l’objet **FormRegion** comme exemple, la liste suivante examine ce que contient chaque interface et classe répertoriées précédemment.</span><span class="sxs-lookup"><span data-stu-id="70590-114">Continuing to use the **FormRegion** object as an example, the following list examines what each interface and class listed earlier contains.</span></span>

- <span data-ttu-id="70590-115">L'interface \_FormRegion définit toutes les méthodes et propriétés de l'objet FormRegion.</span><span class="sxs-lookup"><span data-stu-id="70590-115">The \_FormRegion interface defines all the methods and properties of FormRegion.</span></span> <span data-ttu-id="70590-116">Vous n’utiliserez généralement pas cette interface dans le code, à l’exception d’une des conditions décrite ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="70590-116">Typically you do not use this interface in code, except for a condition discussed below.</span></span>

- <span data-ttu-id="70590-117">L'interface **FormRegionEvents** définit des méthodes qui sont mappées à des événements de FormRegion.</span><span class="sxs-lookup"><span data-stu-id="70590-117">The **FormRegionEvents** interface defines methods mapping to events of FormRegion.</span></span> <span data-ttu-id="70590-118">Vous n’utiliserez pas cette interface dans le code.</span><span class="sxs-lookup"><span data-stu-id="70590-118">You do not use this interface in code.</span></span>

- <span data-ttu-id="70590-119">L'outil TLBIMP approfondit le traitement de l'interface **FormRegionEvents** de manière à créer l'interface **FormRegionEvents**\_Event qui définit tous les événements de FormRegion.</span><span class="sxs-lookup"><span data-stu-id="70590-119">TLBIMP further processes the **FormRegionEvents** interface to create the **FormRegionEvents**\_Event interface that defines all the events of FormRegion.</span></span> <span data-ttu-id="70590-120">Vous n’utiliserez généralement pas cette interface dans le code, à l’exception d’une des conditions décrite ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="70590-120">Typically you do not use this interface in code, except for a condition discussed below.</span></span>

- <span data-ttu-id="70590-p105">La classe FormRegionClass définit tous les membres (méthodes, propriétés et événements) de FormRegion. Il s'agit de la classe qui est associée à l'interface FormRegion en arrière-plan afin que vous puissiez écrire du code pour créer une instance de l'interface FormRegion. Toutefois, vous n'utilisez pas cette interface directement dans le code.</span><span class="sxs-lookup"><span data-stu-id="70590-p105">The FormRegionClass class defines all the method, property, and event members of FormRegion. This is the class that the FormRegion interface is attributed to associate with behind the scenes so that you can write code to create an instance of the FormRegion interface. However, you do not use this interface directly in code.</span></span>

- <span data-ttu-id="70590-124">L'interface FormRegion hérite des interfaces \_FormRegion et **FormRegionEvents**\_Event.</span><span class="sxs-lookup"><span data-stu-id="70590-124">The FormRegion interface inherits the \_FormRegion interface and the **FormRegionEvents**\_Event interface.</span></span> <span data-ttu-id="70590-125">La figure 1 illustre cette relation d’héritage.</span><span class="sxs-lookup"><span data-stu-id="70590-125">Figure 1 illustrates this inheritance relationship.</span></span>
    
  <span data-ttu-id="70590-126">**Figure 1. L'interface FormRegion hérite des méthodes et des propriétés de l'interface \_FormRegion et hérite des événements de l'interface FormRegionEvents\_Event**</span><span class="sxs-lookup"><span data-stu-id="70590-126">**Figure 1. The FormRegion interface inherits methods and properties from the \_FormRegion interface, and inherits events from the FormRegionEvents\_Event interface**</span></span>

  ![L'interface FormRegion hérite des méthodes et des propriétés de l'interface _FormRegion et hérite des événements de l'interface FormRegionEvents_Event](media/pia-form-region-interface.gif)
    
  <span data-ttu-id="70590-128">D’une manière générale, FormRegion est la seule interface que vous utilisez dans le code managé pour accéder à l’objet et aux membres (méthodes, propriétés et événements) de l’objet **FormRegion**.</span><span class="sxs-lookup"><span data-stu-id="70590-128">Typically, FormRegion is the one interface you use in managed code to access the object and the method, property, and event members of the **FormRegion** object.</span></span>

<span data-ttu-id="70590-p107">Si l'objet **Application** est maintenant utilisé comme exemple, vous accédez aux objets, méthodes, propriétés et événements de l'objet **Application** via l'interface [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) . Il existe néanmoins trois exceptions pour lesquelles vous devez utiliser une autre interface, ou en fonction du langage, vous voudrez utiliser une autre interface :</span><span class="sxs-lookup"><span data-stu-id="70590-p107">Using the **Application** object as another example, you access the **Application** object, methods, properties, and events through the [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) interface. There are however three exceptions where you must use a different interface, or depending on the language, you would want to use a different interface:</span></span>

- <span data-ttu-id="70590-131">Lorsque vous accédez à une méthode qui partage le même nom qu'un événement, il est conseillé d'effectuer un cast en interface principale pour appeler la méthode.</span><span class="sxs-lookup"><span data-stu-id="70590-131">When you access a method that shares the same name as an event, a good practice is to cast to the primary interface to call the method.</span></span> <span data-ttu-id="70590-132">Par exemple, l’objet **Application** possède une méthode [Quit](https://msdn.microsoft.com/library/bb646614\(v=office.15\)) et un événement [Quit](https://msdn.microsoft.com/library/bb622595\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="70590-132">For example, the **Application** object has a [Quit](https://msdn.microsoft.com/library/bb646614\(v=office.15\)) method and a [Quit](https://msdn.microsoft.com/library/bb622595\(v=office.15\)) event.</span></span> <span data-ttu-id="70590-133">Dans Visual Basic .NET, vous pouvez accéder à la méthode Quit via l’interface Application.</span><span class="sxs-lookup"><span data-stu-id="70590-133">In Visual Basic .NET, you can access the Quit method through the Application interface.</span></span> <span data-ttu-id="70590-134">En C\#, vous pouvez éviter un avertissement du compilateur en effectuant un cast de la méthode Quit en interface principale, comme illustré dans l'exemple de code suivant :</span><span class="sxs-lookup"><span data-stu-id="70590-134">In C\#, you can avoid a compiler warning by casting the Quit method to the primary interface, as shown in the following code sample:</span></span>
    
   ```csharp
      void DemoApp()
      {
          Outlook.Application myApp = new Outlook.Application();
          // Other application code here
          ((Outlook._Application)myApp).Quit();
      }
   ```

- <span data-ttu-id="70590-135">Lorsque vous accédez à un événement qui partage le même nom qu'une méthode de cet objet, vous devez effectuer un cast en interface d'événement appropriée pour vous connecter à l'événement.</span><span class="sxs-lookup"><span data-stu-id="70590-135">When you access an event that shares the same name as a method of that object, you must cast to the appropriate event interface to connect to the event.</span></span> <span data-ttu-id="70590-136">Comme dans l'exemple ci-dessus, pour vous connecter à l'événement Quit, vous effectuez un cast en interface [ApplicationEvents\_11\_Event](https://msdn.microsoft.com/library/bb622725\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="70590-136">Similar to the example above, to connect to the Quit event, you cast to the [ApplicationEvents\_11\_Event](https://msdn.microsoft.com/library/bb622725\(v=office.15\)) interface.</span></span>

- <span data-ttu-id="70590-137">Si vous vous connectez à une version antérieure d'un événement qui a par la suite été étendu dans une version ultérieure d'Outlook, vous devez vous connecter à la version de l'événement dans l'interface antérieure.</span><span class="sxs-lookup"><span data-stu-id="70590-137">When you connect to an earlier version of an event that has been subsequently extended in a later version of Outlook, you must connect to the version of the event in the earlier interface.</span></span> <span data-ttu-id="70590-138">Par exemple, si vous voulez vous connecter à la version de l'événement Quit pour l'objet **Application** implémenté pour Outlook 2002 plutôt qu'à la dernière version, connectez-vous à l'événement [Quit](https://msdn.microsoft.com/library/bb609660\(v=office.15\)) défini dans l'interface [ApplicationEvents\_10\_Event](https://msdn.microsoft.com/library/bb610098\(v=office.15\)), au lieu de l'événement Quit défini dans l'interface ApplicationEvents\_11\_Event.</span><span class="sxs-lookup"><span data-stu-id="70590-138">For example, if you want to connect to the version of the Quit event for the **Application** object implemented for Outlook 2002 instead of the latest version, connect to the [Quit](https://msdn.microsoft.com/library/bb609660\(v=office.15\)) event defined in the [ApplicationEvents\_10\_Event](https://msdn.microsoft.com/library/bb610098\(v=office.15\)) interface, instead of the Quit event defined in the ApplicationEvents\_11\_Event interface.</span></span>

## <a name="see-also"></a><span data-ttu-id="70590-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70590-139">See also</span></span>

- [<span data-ttu-id="70590-140">Mise en rapport de l’assembly PIA Outlook avec le modèle objet</span><span class="sxs-lookup"><span data-stu-id="70590-140">Relating the Outlook PIA with the object model</span></span>](relating-the-outlook-pia-with-the-object-model.md)
- [<span data-ttu-id="70590-141">Objets dans l’assembly PIA Outlook</span><span class="sxs-lookup"><span data-stu-id="70590-141">Objects in the Outlook PIA</span></span>](objects-in-the-outlook-pia.md)
- [<span data-ttu-id="70590-142">Événements dans l'assembly PIA Outlook</span><span class="sxs-lookup"><span data-stu-id="70590-142">Events in the Outlook PIA</span></span>](events-in-the-outlook-pia.md)

