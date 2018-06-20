---
title: Écriture de Code de formulaire Server
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ff33badc-ceed-4364-b99c-8af3af83ceb6
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 860b0150fd1ec66fa8fee387d8d4a96e8bb79761
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787478"
---
# <a name="writing-form-server-code"></a>Écriture de Code de formulaire Server

  
  
**S’applique à**: Outlook 
  
Vous pouvez considérer un serveur de formulaire comme suit : 
  
- Un programme Win32 qui affiche une interface et gère les messages windows par les mécanismes de pompe de message Windows standards.
    
- Objet qui enregistre la fabrique de classe avec OLE et est activé par les méthodes OLE automation.
    
- Un objet MAPI qui suit les règles MAPI pour les interactions avec les autres composants MAPI.
    
 Votre code doit traiter tous les trois de ces exigences large simultanément. 
  
Consultez la section COM et ActiveX Object Services dans le SDK de Windows pour plus d’informations sur l’inscription de fabrique de classe du serveur de votre formulaire. Gestion des messages windows et l’affichage d’une interface sont Windows techniques de programmation standard qui n’ont pas toutes les exigences particulières en ce qui concerne les formulaires MAPI. Là encore, le Kit de développement Windows a plus d’informations sur la programmation Windows. Ce document contient ce que vous devez connaître pour implémenter les interfaces de formulaire MAPI requis et facultatifs afin qu’ils suivent les règles MAPI pour les interactions avec les autres composants MAPI — principalement l’interface MAPI de formulaire manager et les applications de client de messagerie.
  
Toutes les interfaces que vous pouvez utiliser lorsque vous implémentez des serveurs de formulaire sont dérivées, directement ou indirectement, de OLE [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx)de classe de base. Cela signifie que toutes vos mises en œuvre de ces interfaces devra méthodes **QueryInterface**, **AddRef**et **Release** . Vous pouvez vous épargner beaucoup de travail si vous utilisez plusieurs l’héritage des autorisations pour implémenter toutes les interfaces requises dans une nouvelle classe de votre choix, afin que toutes les interfaces que vous utilisez peuvent partager une seule implémentation des méthodes **IUnknown** requis. Pour plus d’informations, voir les méthodes [IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) [IUnknown::QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx)et [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) . Il n’existe aucune considérations spéciales en ce qui concerne les serveurs de formulaire MAPI pour ces méthodes. 
  
Alors que toutes les interfaces de formulaire MAPI sont obligatoires pour tous les serveurs de formulaire, les méthodes de n’importe quelle interface donné sont obligatoires. Autrement dit, si vous choisissez d’implémenter une interface particulière, vous devez implémenter toutes les méthodes dans l’interface. Cette opération diffère de la situation avec d’autres composants MAPI, tel que des transports du message. Heureusement, les méthodes dans les interfaces de formulaire MAPI sont relativement simples, afin que l’implémentation de toutes les ne place une grande charge sur les développeurs.
  
Les interfaces de formulaire MAPI sont indépendants du type de l’outil de développement utilisé pour créer un formulaire de serveur. Cela permet aux formulaires d’être créés à l’aide des outils de développement différents. La seule exigence est que tous les serveurs de formulaire doivent prendre en charge les interfaces de formulaire MAPI requis.
  
Toutes les interfaces MAPI qui sont associées aux formulaires sont requis par tous les serveurs du formulaire. Interfaces facultatives permettent d’implémenter certaines fonctions avancées de formulaire qui ne sont pas nécessaires à la plupart des serveurs de formulaire. Le tableau suivant répertorie les interfaces, qu’ils sont destinés et si vous devez les implémenter.
  
|**Interface**|**Description**|**Status**|
|:-----|:-----|:-----|
|[IMAPIForm : IUnknown](imapiformiunknown.md) <br/> |L’interface principale que les clients utilisent pour la charge des serveurs de formulaire, d’exécuter des verbes formulaire et arrêter les serveurs de formulaire. C’est également l’interface dérivée OLE **IUnknown** utilisé pour informer les autres composants OLE concernant les interfaces implémente un objet form.  <br/> |Obligatoire  <br/> |
|[IPersistMessage : IUnknown](ipersistmessageiunknown.md) <br/> |Utilisé lors du chargement des messages dans et l’enregistrement des messages à partir des objets de formulaire.  <br/> |Obligatoire  <br/> |
|[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md) <br/> |Utilisé par les objets de formulaire pour garder une trace des état de la messagerie client et permettant de savoir si l’objet form est capable d’afficher le message suivant ou précédent dans un dossier.  <br/> |Facultatif  <br/> |
|[IClassFactory](http://msdn.microsoft.com/library/f624f833-2b69-43bc-92cd-c4ecbe6051c5%28Office.15%29.aspx) <br/> |L’interface de fabrique de classe OLE utilisée par les objets de formulaire pour la conformité avec le mécanisme de fabrique de classe OLE.  <br/> |Obligatoire  <br/> |
|[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md) <br/> |Utilisé si votre serveur de formulaire prend en charge plusieurs types de formulaire. Dans ce cas, l’interface **IMAPIFormFactory** permet aux applications clientes accéder aux interfaces **IClassFactory** plusieurs (une par type de formulaire qui prend en charge de votre serveur de formulaire) que le serveur de votre formulaire doit également implémenter.  <br/> |Facultatif  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Développez serveurs de formulaire MAPI](developing-mapi-form-servers.md)

