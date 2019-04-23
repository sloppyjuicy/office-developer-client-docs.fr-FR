---
title: ADO pour Windows Foundation classes (ADO/WFC)
TOCTitle: ADO/WFC
ms:assetid: 73206be8-6515-79e4-e904-cc2d0d59411d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249468(v=office.15)
ms:contentKeyID: 48545628
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: df9def320274df0eb4636aa237deb566dd5725b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281721"
---
# <a name="adowfc"></a><span data-ttu-id="fd24c-102">ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="fd24c-102">ADO/WFC</span></span>


<span data-ttu-id="fd24c-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fd24c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fd24c-p101">ADO for Windows Foundation Classes (ADO/WFC) repose sur le modèle d'événement ADO et présente une API simplifiée. En général, ADO/WFC intercepte les événements ADO, consolide les paramètres de l'événement dans une seule classe d'événements et appelle votre gestionnaire d'événements.</span><span class="sxs-lookup"><span data-stu-id="fd24c-p101">ADO for Windows Foundation Classes (ADO/WFC) builds on the ADO event model and presents a simplified application programming interface. In general, ADO/WFC intercepts ADO events, consolidates the event parameters into a single event class, and then calls your event handler.</span></span>

<span data-ttu-id="fd24c-106">**Pour utiliser les événements ADO dans ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="fd24c-106">**To use ADO events in ADO/WFC**</span></span>

1.  <span data-ttu-id="fd24c-p102">Définissez votre propre gestionnaire d'événements pour traiter un événement. Par exemple, pour traiter l'événement **ConnectComplete** dans la famille **ConnectionEvent**, vous pouvez utiliser ce code :</span><span class="sxs-lookup"><span data-stu-id="fd24c-p102">Define your own event handler to process an event. For example, if you wanted to process the **ConnectComplete** event in the **ConnectionEvent** family, you might use this code:</span></span>
    
    ```java 
     
    public void onConnectComplete(Object sender,ConnectionEvent e) 
    { 
        System.out.println("onConnectComplete:" + e); 
    } 
    ```

2.  <span data-ttu-id="fd24c-p103">Définissez un objet gestionnaire pour représenter votre gestionnaire d'événements. Le type de données de l'objet gestionnaire doit être de type **ConnectEventHandler** pour un événement de type **ConnectionEvent**, ou de type **RecordsetEventHandler** pour un événement de type **RecordsetEvent**. Par exemple, utilisez le code suivant pour votre gestionnaire d'événements **ConnectComplete**:</span><span class="sxs-lookup"><span data-stu-id="fd24c-p103">Define a handler object to represent your event handler. The handler object should be of data type **ConnectEventHandler** for an event of type **ConnectionEvent**, or data type **RecordsetEventHandler** for an event of type **RecordsetEvent**. For example, code the following for your **ConnectComplete** event handler:</span></span>
    
    ```java
        ConnectionEventHandler handler =  
                new ConnectionEventHandler(this, "onConnectComplete"); 
    ```

    <span data-ttu-id="fd24c-p104">Le premier argument du constructeur **ConnectionEventHandler** est une référence à la classe qui contient le gestionnaire d'événements nommé dans le deuxième argument. Le compilateur Microsoft Visual J++ prend également en charge une syntaxe équivalente :</span><span class="sxs-lookup"><span data-stu-id="fd24c-p104">The first argument of the **ConnectionEventHandler** constructor is a reference to the class that contains the event handler named in the second argument. The Microsoft Visual J++ compiler also supports an equivalent syntax:</span></span>
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this, "onConnectComplete"); 
    ```
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this.onConnectComplete); 
    ```
    
    <span data-ttu-id="fd24c-p105">Le premier argument du constructeur **ConnectionEventHandler** est une référence à la classe qui contient le gestionnaire d'événements nommé dans le deuxième argument. Le compilateur Microsoft Visual J++ prend également en charge une syntaxe équivalente :</span><span class="sxs-lookup"><span data-stu-id="fd24c-p105">The first argument of the **ConnectionEventHandler** constructor is a reference to the class that contains the event handler named in the second argument. The Microsoft Visual J++ compiler also supports an equivalent syntax:</span></span>
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this.onConnectComplete); 
    ```
    
    <span data-ttu-id="fd24c-116">L'argument unique est une référence à la classe souhaitée (**this**) et à la méthode dans la classe (**onConnectComplete**).</span><span class="sxs-lookup"><span data-stu-id="fd24c-116">The single argument is a reference to the desired class (**this**) and method within the class (**onConnectComplete**).</span></span>

3.  <span data-ttu-id="fd24c-117">Ajoutez votre gestionnaire d'événements à une liste de gestionnaires chargés de traiter un type particulier d'événement.</span><span class="sxs-lookup"><span data-stu-id="fd24c-117">Add your event handler to a list of handlers designated to process a particular type of event.</span></span> <span data-ttu-id="fd24c-118">Utilisez la méthode avec un nom tel que \**addon \* \* \* EventName*(*handler*).</span><span class="sxs-lookup"><span data-stu-id="fd24c-118">Use the method with a name such as \**addOn\*\*\*EventName*(*handler*).</span></span>

4.  <span data-ttu-id="fd24c-p107">ADO/WFC implémente en interne tous les gestionnaires d'événements ADO. Par conséquent, un événement provoqué par une opération **Connection** ou **Recordset** est intercepté par un gestionnaire d'événements ADO/WFC. Le gestionnaire d'événements ADO/WFC transmet les paramètres **ConnectionEvent** ADO à une instance de la classe **ConnectionEvent** ADO/WFC, ou les paramètres **RecordsetEvent** ADO à une instance de la classe **RecordsetEvent** ADO/WFC. Ces classes ADO/WFC consolident les paramètres d'événement ADO ; autrement dit, chaque classe ADO/WFC contient un membre de données pour chaque paramètre de toutes les méthodes **ConnectionEvent** ou **RecordsetEvent** ADO.</span><span class="sxs-lookup"><span data-stu-id="fd24c-p107">ADO/WFC internally implements all the ADO event handlers. Therefore, an event caused by a **Connection** or **Recordset** operation is intercepted by an ADO/WFC event handler. The ADO/WFC event handler passes ADO **ConnectionEvent** parameters in an instance of the ADO/WFC **ConnectionEvent** class, or ADO **RecordsetEvent** parameters in an instance of the ADO/WFC **RecordsetEvent** class. These ADO/WFC classes consolidate the ADO event parameters; that is, each ADO/WFC class contains one data member for each unique parameter in all the ADO **ConnectionEvent** or **RecordsetEvent** methods.</span></span>

5.  <span data-ttu-id="fd24c-p108">ADO/WFC invoque ensuite votre gestionnaire d'événements dans l'objet d'événement ADO/WFC. Par exemple, votre gestionnaire **onConnectComplete** présente la signature suivante :</span><span class="sxs-lookup"><span data-stu-id="fd24c-p108">ADO/WFC then calls your event handler with the ADO/WFC event object. For example, your **onConnectComplete** handler has a signature like this:</span></span>
    
    ```java 
     
        public void onConnectComplete(Object sender,ConnectionEvent e) 
    ```
    
    <span data-ttu-id="fd24c-125">Le premier argument est le type de l’objet qui a envoyé l’événement ([Connection](connection-object-ado.md) ou [Recordset](recordset-object-ado.md)) et le second argument est l’objet d’événement ADO/WFC (**ConnectionEvent** ou **RecordsetEvent**).</span><span class="sxs-lookup"><span data-stu-id="fd24c-125">The first argument is the type of object that sent the event ([Connection](connection-object-ado.md) or [Recordset](recordset-object-ado.md)), and the second argument is the ADO/WFC event object (**ConnectionEvent** or **RecordsetEvent**).</span></span> <span data-ttu-id="fd24c-126">La signature de votre gestionnaire d'événements est plus simple qu'un événement ADO.</span><span class="sxs-lookup"><span data-stu-id="fd24c-126">The signature of your event handler is simpler than an ADO event.</span></span> <span data-ttu-id="fd24c-127">Cependant, vous devez quand même comprendre le modèle d'événement ADO pour savoir quels paramètres s'appliquent à un événement et comment y répondre.</span><span class="sxs-lookup"><span data-stu-id="fd24c-127">However, you must still understand the ADO event model to know what parameters apply to an event and how to respond.</span></span>

6.  <span data-ttu-id="fd24c-p110">À partir de votre gestionnaire d'événements, revenez au gestionnaire ADO/WFC pour l'événement ADO. ADO/WFC copie les membres de données d'événement ADO/WFC pertinents dans les paramètres d'événement ADO, puis le gestionnaire d'événements ADO revient.</span><span class="sxs-lookup"><span data-stu-id="fd24c-p110">Return from your event handler to the ADO/WFC handler for the ADO event. ADO/WFC copies pertinent ADO/WFC event data members back to the ADO event parameters, and then the ADO event handler returns.</span></span>

7.  <span data-ttu-id="fd24c-130">Lorsque le traitement est terminé, supprimez votre gestionnaire de la liste des gestionnaires d'événements ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="fd24c-130">When you are finished processing, remove your handler from the list of ADO/WFC event handlers.</span></span> <span data-ttu-id="fd24c-131">Utilisez la méthode avec un nom tel que \**RemoveOn \* \* \* EventName*(*handler*).</span><span class="sxs-lookup"><span data-stu-id="fd24c-131">Use the method with a name such as \**removeOn\*\*\*EventName*(*handler*).</span></span>

