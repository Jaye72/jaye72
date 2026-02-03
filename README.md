const treeCount = 5;
                    for (let i = 0; i < treeCount; i++) {
                        const angleOffset = (Math.PI * 2 / treeCount) * i;
                        const time = Date.now() * 0.001;
                        const pulse = Math.sin(time + i) * 0.2 + 0.8;
                        
                        ctx.save();
                        ctx.translate(
                            canvas.width/2 + Math.cos(time * 0.5 + i) * 100,
                            canvas.height/2 + Math.sin(time * 0.5 + i) * 100
                        );
                        drawFractalTree(0, 0, 80 * pulse, -Math.PI/2 + angleOffset + Math.sin(time) * 0.2, 10, 5);
                        ctx.restore();
                    }
