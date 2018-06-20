---
title: Bibliothèque JavaScript et référence REST pour Project Server
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 67b47b8b-d34b-4fad-af49-0c258c345ad2
description: La bibliothèque JavaScript et le reste de référence pour Project Server 2013 contient des informations sur le modèle objet JavaScript et de l’interface REST qui vous permet d’accéder aux fonctionnalités de Project Server. Vous pouvez utiliser ces API pour développer des applications pour les périphériques non Windows qui accèdent à Project Server 2013 et Project Online élargie des navigateurs web applications et compléments Project Professional 2013.
ms.openlocfilehash: f834ffdc80de28eceb2d7ab9b30c1444b0478bd8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787813"
---
# <a name="javascript-library-and-rest-reference-for-project-server"></a>Bibliothèque JavaScript et référence REST pour Project Server

La bibliothèque JavaScript et le reste de référence pour Project Server 2013 contient des informations sur le modèle objet JavaScript et de l’interface REST qui vous permet d’accéder aux fonctionnalités de Project Server. Vous pouvez utiliser ces API pour développer des applications pour les périphériques non Windows qui accèdent à Project Server 2013 et Project Online élargie des navigateurs web applications et compléments Project Professional 2013.
  
> [!NOTE]
> Le modèle objet JavaScript et l’interface REST s’alignent avec le modèle objet côté client de Project Server (CSOM). Elles fournissent une fonctionnalité équivalente à l’espace de noms **Microsoft.ProjectServer.Client** dans le modèle CSOM. 
  
Vous pouvez accéder à des fonctionnalités de Project Server via le modèle objet JavaScript, qui est défini dans l’espace de noms [PS](http://msdn.microsoft.com/library/e3156167-a4fd-1bf6-8d1c-e180de1844ed%28Office.15%29.aspx) dans le `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.js` fichier. L’objet [ProjectContext](http://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx) dans l’espace de noms [PS](http://msdn.microsoft.com/library/e3156167-a4fd-1bf6-8d1c-e180de1844ed%28Office.15%29.aspx) est le point d’entrée pour le modèle objet JavaScript. 
  
> [!NOTE]
> Pour parcourir le modèle objet JavaScript et faciliter le débogage, vous pouvez utiliser le fichier PS.debug.js dans le même répertoire. Pour faciliter le développement sur un ordinateur distant, le [Kit de développement Project 2013 télécharger](https://www.microsoft.com/en-us/download/details.aspx?id=30435) inclut les assemblys .NET Framework pour le modèle CSOM et les fichiers PS.js et PS.debug.js. 
  
Vous pouvez également accéder à des fonctionnalités de Project Server via l’interface REST. Le point d’entrée pour l’interface REST est la ressource **ProjectServer** , auquel vous accédez à l’aide de la `http://ServerName/pwaName/_api/ProjectServer` URI de terminaison. Par exemple, la requête suivante obtient les affectations dans le projet spécifié (remplacez _ServerName_ et _pwaName_et modifiez le GUID correspondant à un projet).
  
`http://ServerName/pwaName/_api/ProjectServer/Projects('263fc8d7-427c-e111-92fc-00155d3ba208')/Assignments`

La ressource **ProjectServer** est décrit dans [les ressources ProjectServer dans l’interface REST](http://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx#bk_ProjectServerResources). Autres ressources REST sont décrits dans la documentation pour les objets JavaScript correspondants et les membres de cette référence. Pour plus d’informations sur l’aide de REST, voir [modèle d’objet côté Client (CSOM) pour Project Server](client-side-object-model-csom-for-project-2013.md) et de la [programmation à l’aide du service REST SharePoint 2013](http://msdn.microsoft.com/en-us/library/fp142385%28office.15%29.aspx).
  
## <a name="javascript-library-and-rest-reference-for-project-server"></a>Bibliothèque JavaScript et référence REST pour Project Server
<a name="pj15_JavaScriptAPIReference_PS"> </a>

- [Référence REST et bibliothèque PS.js JavaScript](http://msdn.microsoft.com/library/5a140021-380a-d9e0-e36d-106df85f56d6%28Office.15%29.aspx) Contient des informations sur le modèle objet JavaScript et de l’interface REST pour Project Server 2013. 
    
## <a name="see-also"></a>Voir aussi
<a name="bk_addresources"> </a>

- [Documentation du développeur Project 2013](project-2013-developer-documentation.md)   
- [Modèle objet côté client (CSOM) pour Project Server](client-side-object-model-csom-for-project-2013.md)   
- [Mise en route avec le modèle objet JavaScript](getting-started-with-the-project-server-2013-javascript-object-model.md)  
- [Travailler avec des projets à l’aide du modèle objet JavaScript](create-retrieve-update-delete-projects-using-project-server-javascript.md)
    

