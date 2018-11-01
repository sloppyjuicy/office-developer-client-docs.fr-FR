---
title: ADO pour Windows Foundation Classes (ADO/WFC)
TOCTitle: ADO/WFC
ms:assetid: 73206be8-6515-79e4-e904-cc2d0d59411d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249468(v=office.15)
ms:contentKeyID: 48545628
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: da01d44e1e681a2de41741b11a9c412181c2fd9e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885079"
---
# <a name="adowfc"></a>ADO/WFC


**S’applique à**: Access 2013, Office 2013

ADO for Windows Foundation Classes (ADO/WFC) repose sur le modèle d'événement ADO et présente une API simplifiée. En général, ADO/WFC intercepte les événements ADO, consolide les paramètres de l'événement dans une seule classe d'événements et appelle votre gestionnaire d'événements.

**Pour utiliser les événements ADO dans ADO/WFC**

1.  Définissez votre propre gestionnaire d'événements pour traiter un événement. Par exemple, pour traiter l'événement **ConnectComplete** dans la famille **ConnectionEvent**, vous pouvez utiliser ce code :
    
    ```java 
     
    public void onConnectComplete(Object sender,ConnectionEvent e) 
    { 
        System.out.println("onConnectComplete:" + e); 
    } 
    ```

2.  Définissez un objet gestionnaire pour représenter votre gestionnaire d'événements. Le type de données de l'objet gestionnaire doit être de type **ConnectEventHandler** pour un événement de type **ConnectionEvent**, ou de type **RecordsetEventHandler** pour un événement de type **RecordsetEvent**. Par exemple, utilisez le code suivant pour votre gestionnaire d'événements **ConnectComplete**:
    
    ```java
        ConnectionEventHandler handler =  
                new ConnectionEventHandler(this, "onConnectComplete"); 
    ```

    Le premier argument du constructeur **ConnectionEventHandler** est une référence à la classe qui contient le gestionnaire d'événements nommé dans le deuxième argument. Le compilateur Microsoft Visual J++ prend également en charge une syntaxe équivalente :
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this, "onConnectComplete"); 
    ```
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this.onConnectComplete); 
    ```
    
    Le premier argument du constructeur **ConnectionEventHandler** est une référence à la classe qui contient le gestionnaire d'événements nommé dans le deuxième argument. Le compilateur Microsoft Visual J++ prend également en charge une syntaxe équivalente :
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this.onConnectComplete); 
    ```
    
    

L'argument unique est une référence à la classe souhaitée (**this**) et à la méthode dans la classe (**onConnectComplete**).


3.  Ajoutez votre gestionnaire d'événements à une liste de gestionnaires chargés de traiter un type particulier d'événement. Utilisez la méthode avec un nom tel que **addOn *** EventName*(*Gestionnaire*).

4.  ADO/WFC implémente en interne tous les gestionnaires d'événements ADO. Par conséquent, un événement provoqué par une opération **Connection** ou **Recordset** est intercepté par un gestionnaire d'événements ADO/WFC. Le gestionnaire d'événements ADO/WFC transmet les paramètres **ConnectionEvent** ADO à une instance de la classe **ConnectionEvent** ADO/WFC, ou les paramètres **RecordsetEvent** ADO à une instance de la classe **RecordsetEvent** ADO/WFC. Ces classes ADO/WFC consolident les paramètres d'événement ADO ; autrement dit, chaque classe ADO/WFC contient un membre de données pour chaque paramètre de toutes les méthodes **ConnectionEvent** ou **RecordsetEvent** ADO.

5.  ADO/WFC invoque ensuite votre gestionnaire d'événements dans l'objet d'événement ADO/WFC. Par exemple, votre gestionnaire **onConnectComplete** présente la signature suivante :
    
    ```java 
     
        public void onConnectComplete(Object sender,ConnectionEvent e) 
    ```
    
    Le premier argument est le type d’objet qui a envoyé l’événement ([Connection](connection-object-ado.md) ou [Recordset](recordset-object-ado.md)) et le deuxième argument est l’objet d’événement ADO/WFC (**ConnectionEvent** ou **RecordsetEvent**). La signature de votre gestionnaire d'événements est plus simple qu'un événement ADO. Cependant, vous devez quand même comprendre le modèle d'événement ADO pour savoir quels paramètres s'appliquent à un événement et comment y répondre.

6.  À partir de votre gestionnaire d'événements, revenez au gestionnaire ADO/WFC pour l'événement ADO. ADO/WFC copie les membres de données d'événement ADO/WFC pertinents dans les paramètres d'événement ADO, puis le gestionnaire d'événements ADO revient.

7.  Lorsque le traitement est terminé, supprimez votre gestionnaire de la liste des gestionnaires d'événements ADO/WFC. Utilisez la méthode avec un nom tel que **removeOn *** EventName*(*Gestionnaire*).

