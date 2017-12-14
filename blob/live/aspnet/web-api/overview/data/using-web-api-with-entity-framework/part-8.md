---
uid: web-api/overview/data/using-web-api-with-entity-framework/part-8
title: Exibir detalhes do Item | Microsoft Docs
author: MikeWasson
description: 
ms.author: aspnetcontent
manager: wpickett
ms.date: 06/16/2014
ms.topic: article
ms.assetid: 75ef94b1-bbec-4681-9210-452dba816144
ms.technology: dotnet-webapi
ms.prod: .net-framework
msc.legacyurl: /web-api/overview/data/using-web-api-with-entity-framework/part-8
msc.type: authoredcontent
ms.openlocfilehash: 0b6ae9384843712cae824ea662b984a40f021e57
ms.sourcegitcommit: 9a9483aceb34591c97451997036a9120c3fe2baf
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2017
---
<a name="display-item-details"></a><span data-ttu-id="3c527-102">Detalhes do Item de exibição</span><span class="sxs-lookup"><span data-stu-id="3c527-102">Display Item Details</span></span>
====================
<span data-ttu-id="3c527-103">por [Mike Wasson](https://github.com/MikeWasson)</span><span class="sxs-lookup"><span data-stu-id="3c527-103">by [Mike Wasson](https://github.com/MikeWasson)</span></span>

[<span data-ttu-id="3c527-104">Baixe o projeto concluído</span><span class="sxs-lookup"><span data-stu-id="3c527-104">Download Completed Project</span></span>](https://github.com/MikeWasson/BookService)

<span data-ttu-id="3c527-105">Nesta seção, você adicionará a capacidade de exibir os detalhes de cada livro.</span><span class="sxs-lookup"><span data-stu-id="3c527-105">In this section, you will add the ability to view details for each book.</span></span> <span data-ttu-id="3c527-106">Em app.js, adicione o seguinte código para o modelo de exibição:</span><span class="sxs-lookup"><span data-stu-id="3c527-106">In app.js, add to the following code to the view model:</span></span>

[!code-javascript[Main](part-8/samples/sample1.js)]

<span data-ttu-id="3c527-107">No Views/Home/Index.cshtml, adicione um elemento de associação de dados para o link de detalhes:</span><span class="sxs-lookup"><span data-stu-id="3c527-107">In Views/Home/Index.cshtml, add a data-bind element to the Details link:</span></span>

[!code-html[Main](part-8/samples/sample2.html?highlight=5)]

<span data-ttu-id="3c527-108">Isso vincula o manipulador de cliques para o &lt;um&gt; elemento para o `getBookDetail` função no modelo de exibição.</span><span class="sxs-lookup"><span data-stu-id="3c527-108">This binds the click handler for the &lt;a&gt; element to the `getBookDetail` function on the view model.</span></span>

<span data-ttu-id="3c527-109">No mesmo arquivo, substitua a seguinte marcação:</span><span class="sxs-lookup"><span data-stu-id="3c527-109">In the same file, replace the following mark-up:</span></span>

[!code-html[Main](part-8/samples/sample3.html)]

<span data-ttu-id="3c527-110">com isso:</span><span class="sxs-lookup"><span data-stu-id="3c527-110">with this:</span></span>

[!code-html[Main](part-8/samples/sample4.html)]

<span data-ttu-id="3c527-111">Essa marcação cria uma tabela que é associado a dados para as propriedades do `detail` observável no modelo de exibição.</span><span class="sxs-lookup"><span data-stu-id="3c527-111">This markup creates a table that is data-bound to the properties of the `detail` observable in the view model.</span></span>

<span data-ttu-id="3c527-112">O "&lt;! – ko -&gt; &quot; sintaxe permite que você incluir uma associação Knockout fora de um elemento DOM.</span><span class="sxs-lookup"><span data-stu-id="3c527-112">The "&lt;!-- ko --&gt;&quot; syntax lets you include a Knockout binding outside of a DOM element.</span></span> <span data-ttu-id="3c527-113">Nesse caso, o `if` associação faz com que esta seção de marcação a ser exibida somente quando `details` não for nulo.</span><span class="sxs-lookup"><span data-stu-id="3c527-113">In this case, the `if` binding causes this section of markup to be displayed only when `details` is non-null.</span></span>

[!code-html[Main](part-8/samples/sample5.html)]

<span data-ttu-id="3c527-114">Agora, se você executa o aplicativo e clique em um do &quot;detalhes&quot; links, o aplicativo exibirá os detalhes de catálogo.</span><span class="sxs-lookup"><span data-stu-id="3c527-114">Now if you run the app and click one of the &quot;Detail&quot; links, the app will display the book details.</span></span>

[![](part-8/_static/image2.png)](part-8/_static/image1.png)

>[!div class="step-by-step"]
<span data-ttu-id="3c527-115">[Anterior](part-7.md)
[Próximo](part-9.md)</span><span class="sxs-lookup"><span data-stu-id="3c527-115">[Previous](part-7.md)
[Next](part-9.md)</span></span>